# Bleed
Add Bleed effect to an element inside a wrapper using calc, Viewport unit and pseudo element


# Solution
```css

.grid--container{
	max-width: 1200px;
	padding: 0 10px;
}

.my-component{
	background-color: black;
	position: relative;

	&:before{
		width: calc(100% + 30px);
		background-color: black;
		position: absolute;
		left: -10px;
		content: '';
		z-index: -1;
		bottom: 0;
		right: 0;
		top: 0;

		@media (min-width: 1200px) {
			left: calc((100vw - 1180px) / 2 * -1  );
			width: 100vw;
		}
	}
}
```

