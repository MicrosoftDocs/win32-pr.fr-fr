---
description: Définition des attributs de type de fichier dans le registre.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Comment définir des attributs de type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864930"
---
# <a name="how-to-define-file-type-attributes"></a><span data-ttu-id="0f172-103">Comment définir des attributs de type de fichier</span><span class="sxs-lookup"><span data-stu-id="0f172-103">How to Define File Type Attributes</span></span>

<span data-ttu-id="0f172-104">L’attribution d’attributs de type de fichier à un ProgID associé vous permet de contrôler certains aspects du comportement du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0f172-104">Assigning file type attributes to an associated ProgID enables you to control some aspects of the file type's behavior.</span></span> <span data-ttu-id="0f172-105">Avant Windows Vista, ces attributs pouvaient vous permettre de limiter la mesure dans laquelle l’utilisateur pouvait utiliser l’onglet de propriétés **Options des dossiers** pour modifier différents aspects du type de fichier, tels que son icône ou ses verbes.</span><span class="sxs-lookup"><span data-stu-id="0f172-105">Prior to Windows Vista, these attributes could enable you to limit the extent to which the user could use the **Folder Options** property tab to modify various aspects of the file type, such as its icon or verbs.</span></span>

<span data-ttu-id="0f172-106">Les attributs de type de fichier sont des indicateurs binaires spécifiés en tant que valeurs **reg \_ DWORD** ou **reg \_ Binary** dans la sous-clé ProgID associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0f172-106">File type attributes are binary flags specified as **REG\_DWORD** or **REG\_BINARY** values in the file type's associated ProgID subkey.</span></span>

<span data-ttu-id="0f172-107">Pour affecter des attributs pour un type de fichier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="0f172-107">To assign attributes for a file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="0f172-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="0f172-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="0f172-109">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="0f172-109">Step 1:</span></span>

<span data-ttu-id="0f172-110">Ajoutez une entrée indicateurs à la sous-clé ProgID associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0f172-110">Add an EditFlags entry to the file type's associated ProgID subkey.</span></span>

### <a name="step-2"></a><span data-ttu-id="0f172-111">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="0f172-111">Step 2:</span></span>

<span data-ttu-id="0f172-112">Affectez à l’entrée la valeur d’attribut appropriée.</span><span class="sxs-lookup"><span data-stu-id="0f172-112">Set the entry to the appropriate attribute value.</span></span>

<span data-ttu-id="0f172-113">L’exemple suivant montre les \_ attributs Association NoRemove (0x00000010) et Association \_ NoNewVerb (0x00000020) définis pour le type de fichier. MYP.</span><span class="sxs-lookup"><span data-stu-id="0f172-113">The following example shows the FTA\_NoRemove (0x00000010) and FTA\_NoNewVerb (0x00000020) attributes set for the .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a><span data-ttu-id="0f172-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0f172-114">Remarks</span></span>

<span data-ttu-id="0f172-115">Les indicateurs peuvent être combinés avec un ou logique pour former la valeur d’attribut unique.</span><span class="sxs-lookup"><span data-stu-id="0f172-115">The flags can be combined with a logical OR to form the single attribute value.</span></span>

<span data-ttu-id="0f172-116">Pour obtenir la liste des attributs de type de fichier possibles et leurs valeurs hexadécimales, ainsi que des détails sur la récupération et la définition par programmation de ces valeurs, consultez [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span><span class="sxs-lookup"><span data-stu-id="0f172-116">For a list of possible file type attributes and their hexadecimal values, and more details on programmatically retrieving and setting these values, see [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span></span>

 

 



