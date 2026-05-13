\subsection{HUD}

\subsubsection*{Diseño general}

El HUD se construye en un \texttt{Canvas} configurado en modo \emph{Scale With Screen Size}. Esta configuración evita deformaciones y permite que la interfaz conserve proporciones adecuadas en diferentes resoluciones de pantalla.

\begin{figure}[h]
    \centering
    \includegraphics[width=0.7\textwidth]{assets/ux/hud.png}
    \caption{Menú principal del videojuego}
    \label{fig:menu}
\end{figure}

\subsubsection*{Elementos principales}

En la esquina superior izquierda se ubica la información vital del jugador. La salud se representa mediante iconos de corazones usando componentes \texttt{UI Image}, acompañados por un contador numérico cuando sea necesario. Cerca de esta zona se muestra el contador de Diamantes de Almas.

\subsubsection*{Textos flotantes de daño}

Cuando un enemigo recibe daño, se instancia un prefab de texto en el espacio del mundo o en un Canvas asociado. Este texto flota hacia arriba y se desvanece progresivamente mediante reducción del valor alfa. La animación puede implementarse con un \texttt{Animator}, una corrutina o un sistema de tweening si el proyecto incorpora una librería externa.

\subsubsection*{Criterios de claridad}

La interfaz debe ser legible sin ocupar espacio excesivo. Los indicadores deben comunicar información esencial y evitar distracciones durante combate o plataformas. La estética debe integrarse con el tono del juego mediante bordes, iconografía y colores coherentes con la fantasía gótica.

