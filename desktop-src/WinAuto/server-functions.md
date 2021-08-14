---
title: fonctions serveur (fonctionnalités d’accessibilité Windows)
description: Fonctions du serveur
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2eb449e81371a1c0c9e230610de97b8abdefb41429c5753059540e45f921d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828067"
---
# <a name="server-functions-windows-accessibility-features"></a>fonctions serveur (fonctionnalités d’accessibilité Windows)

Cette section contient des informations sur les fonctions de serveur utilisées avec Microsoft Active Accessibility.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                     | Description                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | permet à une application de technologie d’assistance d’informer le système qu’elle interagit avec l’interface utilisateur par le biais d’une API d’automatisation de Windows (telle que Microsoft UI automation) suite à un mouvement tactile de l’utilisateur. Cela permet à la technologie d’assistance de notifier l’application cible et le système que l’utilisateur interagit avec Touch.<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Définit des valeurs système qui indiquent si l’état actuel de l’application de technologie d’assistance affecte les fonctionnalités généralement fournies par le système. <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Crée un objet accessible avec les méthodes et les propriétés du type spécifié d’élément d’interface utilisateur fourni par le système.<br/>                                                                                                                                                                                                                      |
| [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Crée un objet accessible qui a les propriétés et les méthodes de la classe spécifiée de l’élément d’interface utilisateur fourni par le système.<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Retourne une référence, semblable à un handle, à l’objet spécifié. Les serveurs retournent cette référence lors du traitement de l’appel de fonction [**\_ GETOBJECT**](wm-getobject.md).<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Récupère un pointeur d’interface demandé pour un objet accessible en fonction d’une référence d’objet précédemment générée.<br/> Cette fonction est conçue pour une utilisation interne par Microsoft Active Accessibility et est documentée à titre d’information uniquement. Ni les clients ni les serveurs ne doivent appeler cette fonction.<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Détermine s’il existe un hook WinEvent installé qui peut être notifié d’un événement spécifié.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Signale au système qu'un événement prédéfini s'est produit. Si une application cliente a inscrit une fonction de raccordement pour l’événement, le système appelle la fonction de raccordement du client.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Active Accessibility les services d’interface utilisateur](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





