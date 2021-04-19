---
title: DataFormats
description: Spécifie les formats de données par défaut et principaux pris en charge par une application.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- La clé de Registre DataFormats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510847"
---
# <a name="dataformats"></a><span data-ttu-id="e3754-104">DataFormats</span><span class="sxs-lookup"><span data-stu-id="e3754-104">DataFormats</span></span>

<span data-ttu-id="e3754-105">Spécifie les formats de données par défaut et principaux pris en charge par une application.</span><span class="sxs-lookup"><span data-stu-id="e3754-105">Specifies the default and main data formats supported by an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e3754-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="e3754-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a><span data-ttu-id="e3754-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e3754-107">Remarks</span></span>

<span data-ttu-id="e3754-108">La valeur *fichier/format* spécifie le format de fichier ou d’objet principal par défaut pour les objets de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e3754-108">The *file/format* value specifies the default main file or object format for objects of this class.</span></span>

<span data-ttu-id="e3754-109">La valeur *formats* spécifie une liste de formats pour les implémentations par défaut de [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), où *n* est un index entier de base zéro.</span><span class="sxs-lookup"><span data-stu-id="e3754-109">The *formats* value specifies a list of formats for default implementations of [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), where *n* is a zero-based integer index.</span></span> <span data-ttu-id="e3754-110">Par exemple, *n*  =  *format*, *aspect*, *moyen*, *indicateur*, où *format* est un format de presse-papiers, *aspect* est un ou plusieurs membres de [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *Medium* est un ou plusieurs membres de [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), et *Flag* est un ou plusieurs membres de [**datadir**](/windows/win32/api/objidl/ne-objidl-datadir).</span><span class="sxs-lookup"><span data-stu-id="e3754-110">For example, *n* = *format*, *aspect*, *medium*, *flag*, where *format* is a clipboard format, *aspect* is one or more members of [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* is one or more members of [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), and *flag* is one or more members of [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3754-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3754-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3754-112">**IDataObject :: EnumFormatEtc**</span><span class="sxs-lookup"><span data-stu-id="e3754-112">**IDataObject::EnumFormatEtc**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[<span data-ttu-id="e3754-113">**IDataObject :: GetData**</span><span class="sxs-lookup"><span data-stu-id="e3754-113">**IDataObject::GetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[<span data-ttu-id="e3754-114">**IDataObject :: SetData**</span><span class="sxs-lookup"><span data-stu-id="e3754-114">**IDataObject::SetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




