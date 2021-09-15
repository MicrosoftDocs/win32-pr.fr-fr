---
title: Écoute des événements de ruban
description: l’infrastructure de ruban Windows utilise l’infrastructure Suivi d’v nements pour Windows (ETW) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Ruban, événements
- Ruban, événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf28052aa741437a7f96f90ddb1b4a773ae4c4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523109"
---
# <a name="listening-for-ribbon-events"></a>Écoute des événements de ruban

l’infrastructure de ruban Windows utilise l’infrastructure [Suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.

## <a name="introduction"></a>Introduction

Le mécanisme d’événement d’infrastructure de ruban est conçu de telle sorte que l’infrastructure signale les événements de l’interface utilisateur du ruban à l’application afin que vous puissiez surveiller l’activité des utilisateurs, apprendre leurs modèles d’interaction et évaluer les tendances d’utilisation. Ces informations peuvent être utilisées pour affiner l’expérience utilisateur des itérations ultérieures de votre application de ruban.

L’utilisation des événements de l’infrastructure du ruban implique les opérations suivantes :

1.  l’application ruban doit inscrire un écouteur de [Suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour recevoir des notifications d’événements de ruban à partir de l’infrastructure du ruban.
2.  l’infrastructure du ruban déclenche des rappels d’événements de l’interface utilisateur du ruban au moment de l’exécution, si l’application a inscrit un écouteur [de Suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) .

## <a name="supported-events"></a>Événements pris en charge

Les événements exposés aux applications du ruban sont décrits dans le tableau suivant. 


| Événement | Rapport d’événements | 
|-------|--------------|
| Onglet activé | ID de commande<br /> Nom de commande<br /> Verbe d’événement<br /> | 
| Onglet contextuel activé | ID de commande<br /> Nom de commande<br /> Verbe d’événement<br /> | 
| Menu de l’application ouvert | Verbe d’événement<br /> | 
| Menu de l’application fermé | Verbe d’événement<br /> | 
| Menu (normal ou Galerie ouvert) | ID de commande<br /> Nom de commande<br /> Verbe d’événement<br /><blockquote>[!Note]<br />Les événements de menu QAT ne sont pas exposés.</blockquote><br /> | 
| Menu (normal ou Galerie fermé) | ID de commande<br /> Nom de commande<br /> Verbe d’événement<br /><blockquote>[!Note]<br />Les événements de menu QAT ne sont pas exposés.</blockquote><br /> | 
| Commande | ID de commande<br /> Nom de commande<br /> Verbe d’événement<br /> L’un des emplacements d’événements suivants :<ul><li>DERNIER</li><li>QUICKACCESSTOOLBAR</li><li>APPLICATIONMENU</li><li>CONTEXTPOPUP</li></ul><br /> ID de commande parent<br /> Nom de la commande parente<br /> L’une des méthodes d’appel suivantes :<ul><li>Cliquez sur</li><li>KEYTIP</li><li>CLAVIER</li><li>INTERFACE</li></ul><br /><blockquote>[!Note]<br />Les galeries d’éléments et les zones de liste déroulante incluent l’index d’élément sélectionné, mais n’incluent pas les valeurs de chaîne et d’entier. Les jointures n’incluent pas la valeur entière.</blockquote><br /> | 
| Ruban réduit | Verbe d’événement<br /> | 
| Ruban développé (bouton de développement cliqué ou appui sur épinglé) | Verbe d’événement<br /> | 
| Mode d’application basculé | Verbe d’événement<br /> ID de mode (valeur définie par <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)<br /><blockquote>[!Note]<br />L’application est chargée de décompresser cet entier pour déterminer les modes qui ont été définis.</blockquote><br /> | 
| Info-bulle affichée | Verbe d’événement<br /> ID de commande parent<br /> Nom de la commande parente<br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Guides du développeur de Framework de ruban](windowsribbon-guides-entry.md)
</dt> <dt>

[Déclaration des commandes et des contrôles avec le balisage du ruban](./windowsribbon-schema.md)
</dt> <dt>

[Instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processus de conception du ruban](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

