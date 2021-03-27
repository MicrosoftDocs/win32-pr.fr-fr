---
description: Montre comment s’assurer que votre application apparaît dans le menu et la boîte de dialogue Ouvrir avec pour les applications de bureau et qu’elle est disponible en tant qu’application du Windows Store par défaut pour les types de fichiers spécifiés.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Comment inclure une application dans la boîte de dialogue Ouvrir avec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864922"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a><span data-ttu-id="4b497-103">Comment inclure une application dans la boîte de dialogue Ouvrir avec</span><span class="sxs-lookup"><span data-stu-id="4b497-103">How to Include an Application in the Open With Dialog Box</span></span>

<span data-ttu-id="4b497-104">Montre comment s’assurer que votre application apparaît dans le menu et la boîte de dialogue **Ouvrir avec** pour les applications de bureau et qu’elle est disponible en tant qu’application du Windows Store par défaut pour les types de fichiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4b497-104">Illustrates how to ensure your application appears in the **Open With** menu and dialog box for desktop apps, and is available as a default Windows Store app for specified file types.</span></span>

## <a name="instructions"></a><span data-ttu-id="4b497-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="4b497-105">Instructions</span></span>

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a><span data-ttu-id="4b497-106">Pour chaque type de fichier, ajoutez votre application à la sous-clé de Registre OpenWithProgIds.</span><span class="sxs-lookup"><span data-stu-id="4b497-106">For each file type, add your application to the OpenWithProgIds registry subkey.</span></span>

<span data-ttu-id="4b497-107">Ajoutez votre ProgID sous la forme d’un nom de valeur, avec le type de valeur REG \_ None ou reg \_ SZ et une chaîne vide comme valeur de données.</span><span class="sxs-lookup"><span data-stu-id="4b497-107">Add your ProgID as a value name, with the value type of either REG\_NONE or REG\_SZ and an empty string as the data value.</span></span>

<span data-ttu-id="4b497-108">Les exemples de registre suivants montrent des entrées qui associent InfoPath et pour Microsoft Visual Studio avec le type de fichier XML.</span><span class="sxs-lookup"><span data-stu-id="4b497-108">The following registry examples show entries associating InfoPath and for Microsoft Visual Studio with the XML file type.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a><span data-ttu-id="4b497-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4b497-109">Remarks</span></span>

<span data-ttu-id="4b497-110">La sous-clé **OpenWithProgids** est préférable à **OpenWithList** pour identifier une application.</span><span class="sxs-lookup"><span data-stu-id="4b497-110">The **OpenWithProgids** subkey is preferred to **OpenWithList** to identify an application.</span></span> <span data-ttu-id="4b497-111">Pour plus d’informations sur ces sous-clés, consultez [définition des sous-clés facultatives et des attributs d’extension de type de fichier](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4b497-111">For more information on these subkeys, see [Setting Optional Subkeys and File Type Extension Attributes](fa-file-types.md).</span></span>

<span data-ttu-id="4b497-112">**OpenWithList** est destiné uniquement aux applications héritées (il doit s’agir de. exe uniquement) sur les systèmes d’exploitation antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b497-112">**OpenWithList** is intended only for legacy apps (must be .exe only) on operating systems prior to Windows XP.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



