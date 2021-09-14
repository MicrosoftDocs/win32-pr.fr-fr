---
description: Négociation des types de médias
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Négociation des types de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223233"
---
# <a name="negotiating-media-types"></a>Négociation des types de médias

quand le gestionnaire de Graph de filtre appelle la méthode [**IPin :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , il dispose de plusieurs options pour spécifier un type de média :

-   **Type complet :** Si le type de média est entièrement spécifié, les broches essaient de se connecter avec ce type. Si ce n’est pas le cas, la tentative de connexion échoue.
-   **Type de média partiel :** Un type de média est *partiel* si le type principal, le sous-type ou le type de format est le GUID \_ null. La valeur du GUID \_ null agit comme un « caractère générique », indiquant que toute valeur est acceptable. Les codes confidentiels négocient un type qui est cohérent avec le type partiel.
-   **Aucun type de média :** si le gestionnaire de Graph de filtre passe un pointeur **NULL** , les broches peuvent accepter tout type de média acceptable pour les deux codes pin.

Si les broches se connectent, la connexion a toujours un type de support complet. l’objectif du type de média donné par le gestionnaire de Graph de filtre est de limiter les types de connexions possibles.

Pendant le processus de négociation, la broche de sortie propose un type de média en appelant la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) du code confidentiel d’entrée. La broche d’entrée peut accepter ou rejeter le type proposé. Ce processus se répète jusqu’à ce que la broche d’entrée accepte un type ou que la broche de sortie manque de types et que la connexion échoue.

La manière dont une broche de sortie sélectionne les types de média à proposer dépend de l’implémentation. dans les classes de base DirectShow, la broche de sortie appelle [**IPin :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) sur la broche d’entrée. Cette méthode retourne un énumérateur qui énumère les types de média préférés du code confidentiel d’entrée. À défaut, la broche de sortie énumère ses propres types préférés.

**Utilisation des types de médias**

Dans toute fonction qui reçoit un paramètre de **\_ \_ type de média am** , validez toujours les valeurs de **cbFormat** et de **formatType** avant de déréférencer le membre **pbFormat** . Le code suivant est incorrect :


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



Le code suivant est correct :


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



