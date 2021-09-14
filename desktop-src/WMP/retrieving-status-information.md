---
title: Récupération des informations d’État
description: Récupération des informations d’État
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Lecteur Windows Media des magasins en ligne, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media des magasins en ligne, récupération de l’état
- magasins en ligne, récupération de l’État
- type 2 magasins en ligne, récupération de l’État
- Lecteur Windows Media, gestionnaire de téléchargement
- Lecteur Windows Media Gestionnaire de téléchargement
- Gestionnaire de téléchargement
- récupération de l’État
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416189"
---
# <a name="retrieving-status-information"></a>Récupération des informations d’État

Les informations d’État sont mises à jour à l’aide de la minuterie créée dans la fonction **init** . Tous les États sont mis à jour à l’aide du même minuteur. Le nom de la fonction pour l’événement du minuteur est **OnTimer**.

**OnTimer** détermine les informations à afficher en fonction de la sélection de l’utilisateur, qui est stockée dans la variable globale nommée g \_ oCurrentDLItem. La fonction teste d’abord si les valeurs de taille ou de progression sont valides et crée une chaîne pour chaque cas.


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



Si une valeur est valide, la chaîne représente le nombre d’octets. Si la valeur n’est pas valide, telle que-1, la chaîne fournit un message pour informer l’utilisateur que les informations ne sont pas encore disponibles.

Ensuite, un bloc **switch** détermine si le téléchargement de l’élément sélectionné est terminé ou annulé. Si l’un ou l’autre cas est true, la valeur de la taille ou de la progression des variables est mise à jour en conséquence.


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



Enfin, les informations d’État s’affichent dans l’élément DIV nommé dlstate.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du gestionnaire de téléchargement**](using-the-download-manager.md)
</dt> </dl>

 

 




