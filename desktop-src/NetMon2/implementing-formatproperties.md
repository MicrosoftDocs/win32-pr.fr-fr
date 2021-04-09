---
description: Moniteur réseau appelle la fonction FormatProperties pour mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implémentation de FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112798"
---
# <a name="implementing-formatproperties"></a><span data-ttu-id="ea7ae-103">Implémentation de FormatProperties</span><span class="sxs-lookup"><span data-stu-id="ea7ae-103">Implementing FormatProperties</span></span>

<span data-ttu-id="ea7ae-104">Moniteur réseau appelle la fonction [**FormatProperties**](formatproperties.md) pour mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-104">Network Monitor calls the [**FormatProperties**](formatproperties.md) function to format the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="ea7ae-105">En règle générale, **FormatProperties** est appelé pour mettre en forme la ligne de résumé pour un protocole, puis pour mettre en forme toutes les instances de propriété du protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-105">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="ea7ae-106">Toutefois, Moniteur réseau n’identifie pas le nombre de fois où **FormatProperties** est appelé pour un analyseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-106">However, Network Monitor does not identify the number of times that **FormatProperties** is called for a specific parser.</span></span>

<span data-ttu-id="ea7ae-107">Lors de l’appel de [**FormatProperties**](formatproperties.md), moniteur réseau fournit une structure [**PROPERTYINST**](propertyinst.md) pour chaque propriété qu’il affiche.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-107">When calling [**FormatProperties**](formatproperties.md), Network Monitor provides a [**PROPERTYINST**](propertyinst.md) structure for each property that it displays.</span></span> <span data-ttu-id="ea7ae-108">La structure **PROPERTYINST** fournit des informations sur les données à afficher, y compris un pointeur vers la structure [**PROPERTYINFO**](propertyinfo.md) qui spécifie la fonction à utiliser pour mettre en forme la propriété de données affichée.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-108">The **PROPERTYINST** structure provides information about the data to be displayed, including a pointer to the [**PROPERTYINFO**](propertyinfo.md) structure that specifies the function to use to format the displayed data property.</span></span>

> [!Note]  
> <span data-ttu-id="ea7ae-109">Une structure [**PROPERTYINFO**](propertyinfo.md) est spécifiée lors de l’ajout d’une propriété à la [*base de données des propriétés*](p.md) de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-109">A [**PROPERTYINFO**](propertyinfo.md) structure is specified when adding a property to the [*property database*](p.md) of the parser.</span></span>

 

<span data-ttu-id="ea7ae-110">Moniteur réseau identifie la fonction de format à appeler pour chaque instance de propriété.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-110">Network Monitor identifies the format function to call for each property instance.</span></span> <span data-ttu-id="ea7ae-111">Le membre **InstanceData** de la structure [**PROPERTYINFO**](propertyinfo.md) peut spécifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ea7ae-111">The **InstanceData** member of the [**PROPERTYINFO**](propertyinfo.md) structure can specify the following:</span></span>

-   <span data-ttu-id="ea7ae-112">Fonction [**FormatPropertyInstance**](formatpropertyinstance.md) pour utiliser le [*formateur générique*](g.md) fourni par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-112">The [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the [*generic formatter*](g.md) that Network Monitor provides.</span></span>

    <span data-ttu-id="ea7ae-113">– ou –</span><span class="sxs-lookup"><span data-stu-id="ea7ae-113">– or –</span></span>

-   <span data-ttu-id="ea7ae-114">Nom d’une fonction de format personnalisé fournie par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-114">The name of a custom format function that the parser provides.</span></span>

<span data-ttu-id="ea7ae-115">Les fonctions [**FormatPropertyInstance**](formatpropertyinstance.md) et format personnalisé retournent les données mises en forme qui s’affichent dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-115">The [**FormatPropertyInstance**](formatpropertyinstance.md) and the custom format functions return the formatted data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="ea7ae-116">L’illustration suivante montre comment Moniteur réseau identifie la fonction à appeler pour chaque instance de propriété.</span><span class="sxs-lookup"><span data-stu-id="ea7ae-116">The following illustration shows how Network Monitor identifies the function to call for each property instance.</span></span>

![Comment le moniteur réseau identifie la fonction à appeler](images/formatprop1.png)

<span data-ttu-id="ea7ae-118">La procédure suivante identifie les étapes nécessaires à l’implémentation de [**FormatProperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="ea7ae-118">The following procedure identifies the steps necessary to implement [**FormatProperties**](formatproperties.md).</span></span>

<span data-ttu-id="ea7ae-119">**Pour implémenter FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="ea7ae-119">**To implement FormatProperties**</span></span>

-   <span data-ttu-id="ea7ae-120">À l’aide d’une structure de boucle, appelez la fonction format pour chaque structure [**PROPERTYINST**](propertyinst.md) transmise à l’analyseur dans le paramètre *lpPropInst* de la fonction [**FormatProperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="ea7ae-120">Using a loop structure, call the format function for each [**PROPERTYINST**](propertyinst.md) structure that is passed to the parser in the *lpPropInst* parameter of the [**FormatProperties**](formatproperties.md) function.</span></span>

<span data-ttu-id="ea7ae-121">Voici une implémentation de base de [**FormatProperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="ea7ae-121">The following is a basic implementation of [**FormatProperties**](formatproperties.md).</span></span>

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



