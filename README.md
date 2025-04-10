<svg fill="none" viewBox="0 0 600 300" width="600" height="300" xmlns="http://www.w3.org/2000/svg">
  <foreignObject width="100%" height="100%">
    <div xmlns="http://www.w3.org/1999/xhtml">
      <style>
        .false-shadow {
            --shadow-offset: 10px;
            position: relative;
            border: none;
            padding: var(--shadow-offset);
            transition: padding 0.2s;
            z-index: 0;
        }
        
        .false-shadow::before,
        .false-shadow::after
        {
            content: "";
            position: absolute;
            inset: 0;
            isolation: isolate;
            z-index: -1;
            border: var(--shadow-border); /* no default value for --shadow-border */
            border-radius: inherit;
            background-color: var(--color-1-bg);
            transition: transform 0.2s, background-color 1s;
        }
        
        .false-shadow,
        .false-shadow.hoverable:hover,
        .false-shadow.clickable
        {
            padding: calc(var(--shadow-offset) * 2);
            padding-left: 0;
            padding-top: 0;
        }
        
        .false-shadow.hoverable,
        .false-shadow.clickable:active {
            padding: var(--shadow-offset);
        }
        
        .false-shadow::before,
        .false-shadow.hoverable:hover::before,
        .false-shadow.clickable::before
        {
            transform: translate(var(--shadow-offset), var(--shadow-offset));
        }
        
        .false-shadow::after,
        .false-shadow.hoverable:hover::after,
        .false-shadow.clickable::after {
            transform: translate(calc(-1 * var(--shadow-offset)), calc(-1 * var(--shadow-offset)));
        }
        
        .false-shadow.hoverable::before,
        .false-shadow.clickable:active::before
        {
            transform: translate(0,0);
            background-color: var(--color-1);
        }
        
        .false-shadow.hoverable::after,
        .false-shadow.clickable:active::after
        {
            transform: translate(0,0);
        }
        
        .solid-shadow::before {
            background: var(--color-1);
        }
        
        .line-shadow::before {
            opacity: 0.8;
            background-size: 10px 10px;
            background-image: repeating-linear-gradient(45deg, var(--color-1) 0, var(--color-1) 1px, transparent 0, transparent 50%);
        }
        
        .dot-shadow::before {
            opacity: 0.8;
            background-size: 10px 10px;
            background-image: radial-gradient(var(--color-1) 2px, transparent 2px);
        }
      </style>
        <div class="false-shadow solid-shadow">
            <section>I am a self-taught software engineer with over a year of industry experience. In my freetime I build everything from Chrome extensions to Unity games, but my professional focus is on full-stack web development. My journey into tech has been driven by curiosity and a love for creating innovative solutions</section>
            <section>Before I discovered a professional interest in programming, I was working in the field of clinical research. I have always loved to work with people, and with organizations that I believe are contributing to the common good. I am eager to bring my diverse skill set and enthusiasm to a purpose-driven development team.</section>
        </div>
    </div>
  </foreignObject>
</svg>
