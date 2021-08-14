---
title: DataFormats
description: Spécifie les formats de données par défaut et principaux pris en charge par une application.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- La clé de Registre DataFormats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb8b2cc2ad4d11137fa41f419db2184f1a2b47fb850176227401e3d2b1aec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310597"
---
# <a name="dataformats"></a>DataFormats

Spécifie les formats de données par défaut et principaux pris en charge par une application.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>Remarques

La valeur *fichier/format* spécifie le format de fichier ou d’objet principal par défaut pour les objets de cette classe.

La valeur *formats* spécifie une liste de formats pour les implémentations par défaut de [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), où *n* est un index entier de base zéro. Par exemple, *n*  =  *format*, *aspect*, *moyen*, *indicateur*, où *format* est un format de presse-papiers, *aspect* est un ou plusieurs membres de [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *Medium* est un ou plusieurs membres de [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), et *Flag* est un ou plusieurs membres de [**datadir**](/windows/win32/api/objidl/ne-objidl-datadir).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IDataObject :: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject :: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject :: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




