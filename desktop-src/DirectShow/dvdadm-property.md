---
description: La propriété DVDAdm fournit l’accès à l’objet MSDVDAdm qui contient des méthodes et des propriétés pour l’enregistrement des informations sur l’application et l’utilisateur.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Propriété DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adedea036393e68456cfd9f035882ae9c335063030518e808c57bced6d5b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079159"
---
# <a name="dvdadm-property"></a>Propriété DVDAdm

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm` propriété fournit l’accès à l’objet [MSDVDAdm](msdvdadm-object.md) qui contient des méthodes et des propriétés pour l’enregistrement des informations sur l’application et l’utilisateur.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Il n’est pas nécessaire de créer une référence distincte à l’objet **MSDVDAdm** . Pour accéder aux méthodes et aux propriétés de l’objet, utilisez la `DVDAdm` propriété comme indiqué dans l’exemple suivant.

## <a name="examples"></a>Exemples


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



