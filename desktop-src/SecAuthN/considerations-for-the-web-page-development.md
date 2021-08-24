---
description: Le Service Broker d’authentification Web est basé sur les technologies qui alimentent Internet Explorer Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Considérations sur le développement de pages web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22932f40d5268059fc30e97817de0b3671cee7447974b038ea4be12eedd76ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883250"
---
# <a name="considerations-for-the-web-page-development"></a>Considérations sur le développement de pages web

Le Service Broker d’authentification Web est basé sur les technologies qui alimentent Internet Explorer Windows. Toutefois, en raison d’un objectif très spécial de ce composant, certaines fonctionnalités d’Internet Explorer ont été désactivées ou verrouillées à une configuration spécifique. En outre, le Service Broker d’authentification Web fournit un canal de journalisation des événements dédié pour aider à résoudre les problèmes liés aux pages qu’il traite.

## <a name="internet-explorer-10-standard-document-mode"></a>Internet Explorer 10 le mode de document standard

Le Service Broker d’authentification Web affiche toutes les pages en « IE10 standard mode ». Vous pouvez utiliser les outils de développement dans Internet Explorer pour voir comment votre page fonctionne dans différents modes de document. pour plus d’informations sur la compatibilité de Internet Explorer 10, consultez les rubriques MSDN pour [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Fonctionnalités désactivées et verrouillées

Plusieurs fonctionnalités d’Internet Explorer sont complètement désactivées ou verrouillées vers des valeurs spécifiques qui ne peuvent pas être modifiées dans les options Internet du système d’exploitation.



| Fonctionnalité                            | Statut                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API du cache d’application (« AppCache) ») | Désactivé                                                                                                                                                                                                        |
| Historique des liens                       | Désactivé                                                                                                                                                                                                        |
| Fichiers temporaires                    | activé                                                                                                                                                                                                         |
| Cookies                            | Les cookies de session sont activés. Les cookies persistants sont autorisés, mais ils sont soumis au nettoyage automatique, sauf si le répartiteur d’authentification Web est en mode SSO. Pour plus d’informations, consultez la section authentification unique. |
| BASE de l’index                           | Désactivé                                                                                                                                                                                                        |
| Stockage DOM                        | Désactivé                                                                                                                                                                                                        |
| ActiveX                            | Désactivé                                                                                                                                                                                                        |
| Téléchargements de fichiers                     | Désactivé                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>Configuration requise pour HTTPs

La première URL qu’une application doit utiliser pour communiquer avec le fournisseur en ligne doit être HTTPs.

## <a name="dimension-for-different-window-sizes"></a>Dimension pour différentes tailles de fenêtre

une application Windows 8 peut apparaître dans différentes tailles, par exemple plein écran, une fenêtre redimensionnée ou une icône de partage. En fonction de la disposition de fenêtre affichée par le répartiteur d’authentification Web, la taille avec laquelle les pages Web doivent fonctionner peut être différente. Pour plus d’informations, consultez la rubrique [instructions pour le redimensionnement des dispositions étroites](/previous-versions/windows/hh465371(v=win.10)) et la rubrique [instructions de partage de contenu](/previous-versions/windows/hh465251(v=win.10)) .

La page Web doit utiliser des requêtes de média CSS pour vérifier la taille à laquelle elle doit travailler et se présenter en conséquence. Toutefois, la page ne doit pas être conçue en fonction des pixels exacts décrits ici et doit être en mesure de s’adapter à différentes tailles. Les tailles spécifiées dans ce document sont susceptibles d’être modifiées dans les versions ultérieures du système d’exploitation.

Si une page ne peut pas contenir toutes les informations de l’espace alloué (par exemple, une longue liste d’autorisations demandées par une application), le répartiteur d’authentification Web fournit des barres de défilement pour permettre à l’utilisateur de faire défiler la page en fonction des besoins. Le zoom est également fourni par pincer pour les appareils tactiles et CTRL + roulette de la souris pour les PC de bureau et les ordinateurs portables.

pour tester différents facteurs de mise à l’échelle, utilisez l ['exemple d’application du kit de développement logiciel (SDK) Web authentication Broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) chargée dans Microsoft Visual Studio Professional 2012 qui permet de simuler les états en plein écran et redimensionnés.

Outre les différentes dispositions documentées ci-dessus, veillez à tester votre page dans une autre orientation d’écran (par exemple, portrait et paysage), ainsi que des paramètres régionaux et des langages différents, ainsi que des fonctionnalités d’accessibilité telles que l’option « rendre tout le plus grand » activée.

Les dispositions disponibles sont les suivantes :

-   [Plein écran](#full-screen)
-   [Fenêtre redimensionnée](#resized)
-   [Vue de l’icône](#charm-view)
-   [Vue du sélecteur de fichiers](#file-picker-view)

### <a name="full-screen"></a>Plein écran

Pour la disposition plein écran, les dimensions de la page Web sont les suivantes :

-   Largeur : 566 pixels
-   Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)

L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web en mode plein écran.

![exemple d’interface utilisateur du Broker d’authentification Web en mode plein écran](images/wab-figure2.png)

### <a name="resized"></a>Redimensionné

Pour une fenêtre redimensionnée, les dimensions de la page Web peuvent être :

-   Largeur : 260 pixels
-   Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)

L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web dans une fenêtre redimensionnée sur la page Web XBox. Notez que l’interface utilisateur du répartiteur d’authentification Web se trouve uniquement sur le côté droit de la capture d’écran.

![exemple d’interface utilisateur du Broker d’authentification Web dans une fenêtre redimensionnée](images/wab-figure3.png)

### <a name="charm-view"></a>Vue de l’icône

Pour la vue de l’icône, les dimensions de la page Web sont les suivantes :

-   Largeur : 566 pixels
-   Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)

L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web dans la vue icône.

![un exemple illustre l’interface utilisateur du répartiteur d’authentification Web dans la vue icône](images/wab-figure4.png)

### <a name="file-picker-view"></a>Vue du sélecteur de fichiers

Pour la vue sélecteur de fichiers, les dimensions de la page Web sont les suivantes :

-   Largeur : 566 pixels
-   Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)

L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web dans la vue sélecteur de fichiers.

![un exemple illustre l’interface utilisateur du Service Broker d’authentification Web dans la vue sélecteur de fichiers](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>Aucune nouvelle fenêtre par défaut

Par défaut, aucune URL n’entraîne l’ouverture d’une nouvelle fenêtre, mais elle s’affiche à la place dans la fenêtre du répartiteur d’authentification Web. Cela comprend la méthode JavaScript window. Open, l’attribut « Target » des liens hypertexte ou lorsque l’utilisateur utilise le mécanisme Ctrl + clic pour forcer l’ouverture d’une nouvelle fenêtre. La seule exception à cette règle est lorsqu’une page Web déclare un lien comme étant sécurisé pour naviguer dans un navigateur, comme décrit dans la cible de personnalisation des liens hypertexte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple d’application du SDK du Broker d’authentification Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
