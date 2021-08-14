---
description: Les exemples suivants utilisent la fonction SetStringInBlob pour créer des entrées d’objet BLOB spéciales.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Entrées d’objets BLOB spéciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0659fa05219dcc715c6c00b3d28635e2500f73e4e5bece72049ee43839a0820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363137"
---
# <a name="special-blob-entries"></a>Entrées d’objets BLOB spéciales

Les exemples suivants utilisent la fonction [**SetStringInBlob**](setstringinblob.md) pour créer des entrées d’objet BLOB spéciales.

## <a name="npp-name"></a>Nom du NPP

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a>Identificateur de classe NPP

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a>Nom de la procédure CFGPROC

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a>Nom de la racine de l’arborescence pour l’interface utilisateur du Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a>Chaîne d’affichage pour l’interface utilisateur du Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a>Balises d’interface

Cet exemple comprend toutes les interfaces prises en charge par le NPP.

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



