<script>
    export let icon;
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
  </script>
  
  <div class="icon" on:dblclick={() => dispatch('click')}>
    <div class="icon-image">{icon.icon}</div>
    <div class="icon-name">{icon.name}</div>
  </div>
  
  <style>
    .icon {
      width: 80px;
      text-align: center;
      cursor: pointer;
      color: white;
    }
  
    .icon-image {
      font-size: 32px;
      margin-bottom: 5px;
    }
  
    .icon-name {
      font-size: 12px;
      word-wrap: break-word;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.8);
    }
  
    .icon:hover {
      background: rgba(255,255,255,0.1);
      border-radius: 5px;
    }
  </style>