---
Description : pour accéder aux données de compteur sur un ordinateur distant : le service d’accès à distance au registre doit être activé sur l’ordinateur distant. l’exception de partage de fichiers et d’imprimantes doit être sélectionnée dans Windows Paramètres de pare-feu. avant Windows Vista : le service d’accès à distance au registre est activé par défaut.
ms. AssetID : 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title : accès aux données des compteurs distants ms. topic : article ms. Date : 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Accès aux données des compteurs distants

Pour accéder aux données de compteur sur un ordinateur distant :

- Le service d’accès à distance au registre doit être activé sur l’ordinateur distant.
- l’exception de **partage de fichiers et d’imprimantes** doit être sélectionnée dans **Windows Paramètres de pare-feu**.

**avant Windows Vista :** Le service d’accès à distance au registre est activé par défaut.

> [!NOTE]
> Windows Les API et les outils du compteur de performances incluent une prise en charge limitée de l’accès aux compteurs de performances à partir d’autres ordinateurs via RPC (pour les fournisseurs v2) et le Registre distant (pour les fournisseurs v1). Cette prise en charge est souvent difficile à utiliser en termes de contrôles d’authentification (les outils et les API peuvent uniquement s’authentifier en tant qu’utilisateur actuel), ainsi qu’en termes de configuration du système (les points de terminaison et les services nécessaires sont désactivés par défaut sur la plupart des systèmes). Dans de nombreux cas, il est préférable d’accéder aux compteurs de performance des systèmes distants via [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) plutôt qu’à l’aide de la prise en charge intégrée de l’accès à distance.
