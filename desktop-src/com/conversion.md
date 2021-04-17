---
title: Conversion
description: Utilisé par la boîte de dialogue Convertir pour déterminer les formats qu’une application peut lire et écrire.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Conversion de la clé de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507438"
---
# <a name="conversion"></a><span data-ttu-id="e1c36-104">Conversion</span><span class="sxs-lookup"><span data-stu-id="e1c36-104">Conversion</span></span>

<span data-ttu-id="e1c36-105">Utilisé par la boîte de dialogue **convertir** pour déterminer les formats qu’une application peut lire et écrire.</span><span class="sxs-lookup"><span data-stu-id="e1c36-105">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e1c36-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="e1c36-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a><span data-ttu-id="e1c36-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e1c36-107">Remarks</span></span>

<span data-ttu-id="e1c36-108">Les informations de conversion sont utilisées par la boîte de dialogue **convertir** pour déterminer les formats qu’une application peut lire et écrire.</span><span class="sxs-lookup"><span data-stu-id="e1c36-108">Conversion information is used by the **Convert** dialog box to determine what formats an application can read and write.</span></span> <span data-ttu-id="e1c36-109">Un format de fichier délimité par des virgules est indiqué par un nombre s’il s’agit de l’un des formats de presse-papiers définis dans Windows. h.</span><span class="sxs-lookup"><span data-stu-id="e1c36-109">A comma-delimited file format is indicated by a number if it is one of the Clipboard formats defined in Windows.h.</span></span> <span data-ttu-id="e1c36-110">Une chaîne indique que le format n’est pas défini dans Windows. h (privé).</span><span class="sxs-lookup"><span data-stu-id="e1c36-110">A string indicates the format is not one defined in Windows.h (private).</span></span> <span data-ttu-id="e1c36-111">Dans ce cas, le format lisible et accessible en écriture est \_ plan CF (privé).</span><span class="sxs-lookup"><span data-stu-id="e1c36-111">In this case, the readable and writable format is CF\_OUTLINE (private).</span></span>

<span data-ttu-id="e1c36-112">La valeur *rformat* spécifie le format de fichier qu’une application peut lire (conversion à partir de).</span><span class="sxs-lookup"><span data-stu-id="e1c36-112">The *rformat* value specifies the file format an application can read (convert from).</span></span>

<span data-ttu-id="e1c36-113">La valeur *rwformat* spécifie le format de fichier qu’une application peut lire et écrire (activer en tant que).</span><span class="sxs-lookup"><span data-stu-id="e1c36-113">The *rwformat* value specifies the file format an application can read and write (activate as).</span></span>

 

 




