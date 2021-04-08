---
title: AutoConvertTo
description: Spécifie la conversion automatique d’une classe d’objets donnée en une nouvelle classe d’objets.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Clé de Registre AutoConvertTo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839069"
---
# <a name="autoconvertto"></a><span data-ttu-id="c2c19-104">AutoConvertTo</span><span class="sxs-lookup"><span data-stu-id="c2c19-104">AutoConvertTo</span></span>

<span data-ttu-id="c2c19-105">Spécifie la conversion automatique d’une classe d’objets donnée en une nouvelle classe d’objets.</span><span class="sxs-lookup"><span data-stu-id="c2c19-105">Specifies the automatic conversion of a given class of objects to a new class of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c2c19-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="c2c19-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a><span data-ttu-id="c2c19-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c2c19-107">Remarks</span></span>

<span data-ttu-id="c2c19-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie l’identificateur de classe de l’objet vers lequel l’objet ou la classe d’objets donné doit être converti.</span><span class="sxs-lookup"><span data-stu-id="c2c19-108">This is a **REG\_SZ** value that specifies the class identifier of the object to which the given object or class of objects should be converted.</span></span>

<span data-ttu-id="c2c19-109">Cette clé est généralement utilisée pour convertir automatiquement des fichiers créés par une version antérieure d’une application vers une version plus récente de l’application.</span><span class="sxs-lookup"><span data-stu-id="c2c19-109">This key is typically used to automatically convert files created by an older version of an application to a newer version of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2c19-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2c19-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2c19-111">**OleDoAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="c2c19-111">**OleDoAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[<span data-ttu-id="c2c19-112">**OleGetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="c2c19-112">**OleGetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[<span data-ttu-id="c2c19-113">**OleSetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="c2c19-113">**OleSetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




