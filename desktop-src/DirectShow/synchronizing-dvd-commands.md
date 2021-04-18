---
description: Synchronisation des commandes de DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Synchronisation des commandes de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526289"
---
# <a name="synchronizing-dvd-commands"></a>Synchronisation des commandes de DVD

Les commandes de DVD ne se terminent pas toujours instantanément. Pour cette raison, certaines méthodes de [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sont asynchrones. Celles-ci incluent des méthodes de lecture, telles que **PlayTitle**, et des méthodes de navigation dans les menus, telles que **ShowMenu** et **ReturnFromSubmenu**. Une méthode asynchrone est retournée immédiatement, sans attendre la fin de la commande. Une fois la méthode retournée, d’autres événements peuvent empêcher l’exécution de la commande, même si la méthode a réussi. DirectShow offre plusieurs options de synchronisation des commandes, allant de la synchronisation à la synchronisation complète à l’aide d’événements de graphique de filtre.

Toutes les méthodes asynchrones ont un paramètre *dwFlags* et un paramètre *ppCmd* . Le paramètre *dwFlags* spécifie le comportement de synchronisation, et le paramètre *ppCmd* retourne un pointeur vers un objet de synchronisation facultatif. Des comportements différents se produisent selon les valeurs que vous donnez à ces paramètres.

**Aucune synchronisation**

Pour une application de lecture de DVD de base, la meilleure option consiste à ignorer les problèmes de synchronisation. Parfois, une commande peut échouer ou l’interface utilisateur peut être légèrement décalée lors de la mise à jour, mais ces erreurs sont de l’ordre des fractions de seconde.

Pour émettre une commande sans synchronisation, définissez l’indicateur DVD \_ cmd \_ \_ None dans le paramètre *dwFlags* et définissez le paramètre *ppCmd* sur la **valeur null**:


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Blocage**

Si vous définissez l' \_ \_ \_ \_ indicateur de bloc d’indicateur cmd DVD cmd dans le paramètre *dwFlags* , la méthode se bloque jusqu’à la fin de l’exécution de la commande :


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



En effet, cet indicateur convertit une méthode asynchrone en méthode synchrone. L’inconvénient est que votre interface utilisateur est bloquée si vous appelez la méthode à partir du thread d’application.

**Objet de synchronisation**

Toutes les méthodes asynchrones peuvent retourner un objet de synchronisation, que vous pouvez utiliser pour attendre le début ou la fin de la commande. Pour récupérer cet objet, transmettez l’adresse d’un pointeur [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) dans le paramètre *ppCmd* :


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Si la méthode est réussie, elle retourne un nouvel objet **IDvdCmd** . La méthode [**IDvdCmd :: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) se bloque jusqu’à ce que la commande commence, et la méthode [**IDvdCmd :: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) se bloque jusqu’à la fin de la commande. La valeur de retour indique l’état de la commande.

Le code suivant est fonctionnellement équivalent à la définition de \_ l' \_ indicateur de bloc d’indicateur cmd DVD cmd \_ \_ , indiqué précédemment.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



Dans ce cas, la méthode **PlayTitle** n’est pas bloquée, mais l’application bloque en appelant **WaitForEnd**.

**Événements d’état de la commande**

Si vous définissez l' \_ \_ \_ indicateur SendEvents de l’indicateur de commande de DVD dans le paramètre *DWFLAGS* , le navigateur DVD envoie un événement de démarrage de la commande de DVD de l’ensemble des DVD lors du [**\_ \_ \_ démarrage**](ec-dvd-cmd-start.md) de la commande et un événement de fin de la commande de [**\_ DVD \_ cmd \_**](ec-dvd-cmd-end.md) à la fin de la commande.

Le paramètre *lParam2* de l’événement est la valeur de retour HRESULT pour la commande. Le paramètre *lParam1* de l’événement permet d’obtenir l’objet de synchronisation pour la commande. Si vous transmettez *lParam1* à la méthode [**IDvdInfo2 :: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , la méthode retourne un pointeur vers l’interface **IDvdCmd** de l’objet de synchronisation. Vous pouvez utiliser cette interface pour attendre la fin de la commande, comme décrit précédemment. Toutefois, si vous avez passé **null** pour le paramètre *ppCmd* dans la méthode **IDvdControl2** d’origine, le navigateur DVD ne crée pas d’objet de synchronisation, et **GetCmdFromEvent** retourne E \_ Fail.

Le code suivant montre comment utiliser des événements d’état de commande sans objet de synchronisation.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



Notez que sans objet de synchronisation, vous ne pouvez pas déterminer quelle commande est associée à l’événement. Le code suivant montre comment utiliser des événements avec l’objet de synchronisation. L’idée est de stocker les objets de synchronisation dans une liste, puis de comparer les pointeurs d’objet lorsque vous obtenez l’événement de fin [**de la commande de DVD ou de \_ \_ \_**](ec-dvd-cmd-start.md) fin de la [**\_ \_ commande \_ de DVD**](ec-dvd-cmd-end.md) de l’EC.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



**Vidage des mémoires tampons du navigateur DVD**

Pendant la lecture, le navigateur DVD met en mémoire tampon les données vidéo. La quantité de données mises en mémoire tampon varie. Lorsque le navigateur DVD bascule sur un nouveau morceau de vidéo, les données qui se trouvent déjà dans le pipeline ne sont pas perdues, donc la transition est transparente. Par défaut, lorsque le navigateur DVD émet une commande, il ne vide pas les données qui se trouvent déjà dans le pipeline. Par conséquent, il peut y avoir une certaine latence avant que vous puissiez voir l’effet de la commande, en fonction de la quantité de données mises en mémoire tampon. Pour augmenter la réactivité, vous pouvez forcer le vidage du navigateur DVD en définissant l' \_ indicateur de vidage de l’indicateur de commande DVD cmd \_ \_ .


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Cet indicateur peut être combiné avec l’un des indicateurs décrits précédemment, à l’aide d’une opération or au niveau du bit. L’un des effets secondaires du vidage est que certaines vidéos peuvent être perdues. n’utilisez donc pas cet indicateur si vous devez garantir qu’il n’y a pas d’écart dans la vidéo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



