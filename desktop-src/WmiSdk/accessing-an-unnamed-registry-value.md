---
description: Accès à une valeur de registre sans nom
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Accès à une valeur de registre sans nom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538937"
---
# <a name="accessing-an-unnamed-registry-value"></a><span data-ttu-id="68219-103">Accès à une valeur de registre sans nom</span><span class="sxs-lookup"><span data-stu-id="68219-103">Accessing an Unnamed Registry Value</span></span>

<span data-ttu-id="68219-104">La valeur par défaut ou la valeur sans nom d’une clé de Registre est indiquée comme (par défaut) ou <No Name> dans l’éditeur du Registre regedit.</span><span class="sxs-lookup"><span data-stu-id="68219-104">The default, or unnamed value of a registry key is shown as (Default) or <No Name> in the Regedit registry editor.</span></span> <span data-ttu-id="68219-105">Vous pouvez utiliser le fournisseur de Registre système pour accéder à une clé de registre sans nom.</span><span class="sxs-lookup"><span data-stu-id="68219-105">You can use the System Registry provider to access an unnamed registry key.</span></span> <span data-ttu-id="68219-106">De même, vous pouvez également utiliser le fournisseur de Registre système pour accéder aux descriptions des bitmaps, qui sont définies en tant que valeurs sans nom.</span><span class="sxs-lookup"><span data-stu-id="68219-106">Similarly, you can also use the System Registry provider to access bitmap descriptions, which are defined as unnamed values.</span></span>

<span data-ttu-id="68219-107">La procédure suivante décrit comment récupérer une valeur de registre sans nom.</span><span class="sxs-lookup"><span data-stu-id="68219-107">The following procedure describes how to retrieve an unnamed registry value.</span></span>

<span data-ttu-id="68219-108">**Pour récupérer une valeur de registre sans nom**</span><span class="sxs-lookup"><span data-stu-id="68219-108">**To retrieve an unnamed registry value**</span></span>

1.  <span data-ttu-id="68219-109">Définissez une propriété et définissez le qualificateur **PropertyContext** de cette propriété sur une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="68219-109">Define a property and set the **PropertyContext** qualifier of that property to an empty string.</span></span>

    <span data-ttu-id="68219-110">L’exemple de code suivant montre comment la classe définit des propriétés pour stocker des valeurs pour la clé spécifiée par le qualificateur **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="68219-110">The following code example shows how the class defines properties to hold values for the key specified by the **ClassContext** qualifier.</span></span> <span data-ttu-id="68219-111">La valeur par défaut est stockée dans la propriété **par défaut** .</span><span class="sxs-lookup"><span data-stu-id="68219-111">The default value is stored in the **Default** property.</span></span>

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    <span data-ttu-id="68219-112">La clé de transport n’utilise pas la valeur sans nom ; la compilation de ce fichier MOF ne produit donc aucune valeur pour la propriété **par défaut** , sauf si un outil de modification du Registre est utilisé pour modifier la valeur sans nom.</span><span class="sxs-lookup"><span data-stu-id="68219-112">The Transports key does not use the unnamed value, so compilation of this MOF file does not produce any value for the **Default** property unless a registry editing tool is used to change the unnamed value.</span></span>

2.  <span data-ttu-id="68219-113">Pour un fichier bitmap, définissez une propriété et définissez le **PropertyContext** de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="68219-113">For a bitmap file, define a property and set the **PropertyContext** of that property.</span></span>

    <span data-ttu-id="68219-114">L’exemple de code suivant montre comment définir une propriété.</span><span class="sxs-lookup"><span data-stu-id="68219-114">The following code example shows how to define a property.</span></span>

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



