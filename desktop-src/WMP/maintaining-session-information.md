---
title: Gestion des informations de session
description: Gestion des informations de session
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Magasins en ligne du lecteur Windows Media, gestion des informations de session
- magasins en ligne, gestion des informations de session
- type 2 magasins en ligne, gestion des informations de session
- Windows Media Player Online stores, informations de session
- magasins en ligne, informations de session
- type 2 magasins en ligne, informations de session
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- gestion des informations de session
- informations de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311539"
---
# <a name="maintaining-session-information"></a>Gestion des informations de session

## <a name="how-the-sample-stores-information"></a>Comment l’exemple stocke les informations

L’exemple de page Web gère les données à l’aide de cookies. Les cookies sont simplement des paires nom/valeur permanentes que le navigateur Web peut stocker pour vous.

À la fermeture de la page Web, la fonction **Shutdown** s’exécute. **Shutdown** appelle la fonction **SetPendingCookies**. Cette fonction effectue une boucle dans la liste de collection de téléchargements, stockée dans la zone de liste déroulante nommée selDLC. Si une collection de téléchargements contient des éléments incomplets, la fonction appelle la méthode **setcookie**, en passant un nom et une valeur. Pour déterminer la chaîne de nom, vous pouvez ajouter une valeur entière à une valeur constante, **WMPDLC**, qui est stockée dans la variable nommée g \_ sPreCookie. Par exemple, pour la troisième collection de téléchargements en attente, le nom du cookie est « WMPDLC2 », car le mécanisme de comptage est de base zéro. À mesure que chaque cookie est créé, la fonction incrémente la variable globale g \_ en attente pour conserver un nombre de téléchargements en attente. Le code est reproduit ici à des fins pratiques :


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



**IsDLCComplete** est une fonction d’assistance qui effectue simplement une boucle sur chaque élément de téléchargement de la collection de téléchargements pour déterminer si un élément est en attente. S’il existe un élément en attente, la fonction retourne false.

**Setcookie** est la fonction qui crée le cookie.

Quand **SetPendingCookies** retourne, **Shutdown** crée le cookie Count, qui stocke la valeur de la variable g \_ en attente. Cette valeur est importante, car la page Web a besoin d’un moyen de déterminer le nombre de cookies à récupérer lors du rechargement. Le nom du cookie de nombre est stocké dans la variable nommée g \_ sCountCookie.

## <a name="how-the-sample-retrieves-information"></a>Comment l’exemple récupère des informations

Lors du chargement de la page Web, la fonction **init** s’exécute. Tout d’abord, la fonction appelle **GetPendingDlCount** pour récupérer le cookie de nombre. Ensuite, il stocke cette valeur dans la variable nommée g \_ en attente. Ensuite, il appelle la fonction **PopulateDLList** pour récupérer chaque cookie de session de téléchargement et ajouter son identificateur à la zone de liste déroulante. Voici le code de cette fonction :


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



La fonction **ClearList** supprime tous les éléments de la zone de liste.

La fonction entre ensuite dans une boucle. Chaque nom de cookie est généré sous la forme d’une chaîne, puis le cookie est récupéré en appelant la fonction d’assistance **getCookie**. Une fois récupéré, le cookie est supprimé en appelant **DelCookie**. Si le cookie a une valeur, la valeur est ajoutée à la zone de liste. Cette action déclenche l’événement **OnChange** pour la liste selDLC, qui à son tour appelle la fonction de gestionnaire nommée **OnSelectDLC**. Il s’agit de la même fonction que celle qui s’exécute lorsque l’utilisateur sélectionne une collection de téléchargements ; Il s’agit du code qui remplit la zone de liste télécharger l’élément.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du gestionnaire de téléchargement**](using-the-download-manager.md)
</dt> </dl>

 

 




