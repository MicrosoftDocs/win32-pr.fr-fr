---
title: Informations de Registre du fournisseur
description: Cette rubrique montre les clés et les valeurs qui doivent être définies lors de l’ajout d’un fournisseur ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813ad37d77d532e3c9bec91bcc3eda1f0aaf703f09dd3cf1b61ac059d7d7493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838865"
---
# <a name="provider-registry-information"></a>Informations de Registre du fournisseur

Le fournisseur est inscrit auprès d’ADSI avec les clés et valeurs suivantes :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

le fournisseur est inscrit avec Windows avec les clés et valeurs suivantes :

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

l’espace de noms du fournisseur est inscrit avec Windows avec les clés et valeurs suivantes :

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

Dans les paragraphes précédents, le *fournisseur* est l’identificateur de l’objet de niveau supérieur du fournisseur. L' *espace de noms du fournisseur* est l’identificateur de l’objet qui implémente l’espace de noms du fournisseur.

Pour obtenir un exemple spécifique, consultez [installation du composant de l’exemple de fournisseur](installing-the-example-provider-component.md).

 

 




