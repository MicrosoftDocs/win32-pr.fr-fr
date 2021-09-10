---
title: DataFormats
description: Spécifie les formats de données par défaut et principaux pris en charge par une application.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- La clé de Registre DataFormats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363431"
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

 

 




