\subsection{Flujo de navegación}

El sistema de navegación está diseñado para ser cíclico y directo, asegurando que el jugador siempre tenga una ruta clara de regreso a la acción o al menú principal.

\begin{figure}[h]
    \centering
    \includegraphics[width=0.7\textwidth]{assets/ux/logic.png}
    \caption{Menú principal del videojuego}
    \label{fig:menu}
\end{figure}

\subsubsection*{Flujo principal}

El recorrido del usuario sigue una estructura lineal desde el arranque hasta el bucle de juego:

\[
\text{Splash Screen} \rightarrow \text{Main Menu} \rightarrow \text{Core Game} \rightarrow \text{Pause Menu} \rightarrow \text{Game Over / Win Screen}
\]



\subsubsection*{Main Menu}

Funciona como el núcleo de navegación. Desde aquí, el jugador puede gestionar su sesión mediante opciones claras:
\begin{itemize}
    \item \textbf{Play:} Opción principal destacada visualmente para incentivar el inicio inmediato de la partida.
    \item \textbf{About:} Pantalla de información donde se consultan los créditos y detalles técnicos (Unity 6 / C\#).
    \item \textbf{Exit:} Cierre y salida segura de la aplicación.
\end{itemize}

\subsubsection*{Core Game}

Durante el juego activo, la interfaz se simplifica para priorizar la inmersión del jugador, reduciéndose al HUD esencial:
\begin{itemize}
    \item \textbf{HUD:} Visualización dinámica en la esquina superior izquierda que muestra la salud (corazones) y la recolección de recursos (diamantes).
    \item \textbf{Diseño:} Los elementos están posicionados estratégicamente para no obstruir la visión del personaje principal ni de las plataformas de juego.
\end{itemize}

\subsubsection*{Estados finales (Victoria y Derrota)}

Las pantallas de fin de juego cierran el ciclo narrativo y proporcionan retroalimentación inmediata sobre el desempeño:
\begin{itemize}
    \item \textbf{Victory:} Se activa al cumplir los objetivos del nivel. Presenta el mensaje "Victory - Nice, Great Job!" con opciones para avanzar ("Next") o volver al menú.
    \item \textbf{Game Over:} Se activa al perder la salud. Presenta el mensaje "You Lost!!" permitiendo un reintento rápido mediante el botón "Retry" o el retorno al "Menu".
\end{itemize}