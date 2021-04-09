---
title: Attribut de chaîne dans les tableaux
description: Vous pouvez utiliser l’attribut \ String \ pour les tableaux de caractères unidimensionnels, les tableaux à caractères larges et les tableaux d’octets qui représentent des chaînes de texte.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102004"
---
# <a name="the-string-attribute-in-arrays"></a><span data-ttu-id="526b6-104">\[ \] Attribut de chaîne dans les tableaux</span><span class="sxs-lookup"><span data-stu-id="526b6-104">The \[string\] Attribute in Arrays</span></span>

<span data-ttu-id="526b6-105">Vous pouvez utiliser l' \[ [](/windows/desktop/Midl/string) \] attribut de chaîne pour les tableaux de caractères unidimensionnels, les tableaux de caractères larges et les tableaux d’octets qui représentent des chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="526b6-105">You can use the \[ [string](/windows/desktop/Midl/string)\] attribute for one-dimensional character arrays, wide-character arrays, and byte arrays that represent text strings.</span></span> <span data-ttu-id="526b6-106">Si vous utilisez l’attribut de **\[ chaîne \]** , le stub client utilise les fonctions **strlen** ou **wstrlen** de la bibliothèque C pour compter le nombre de caractères de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="526b6-106">If you use the **\[string\]** attribute, the client stub uses the C-library functions **strlen** or **wstrlen** to count the number of characters in the string.</span></span> <span data-ttu-id="526b6-107">Pour éviter des incohérences possibles, MIDL ne vous permet pas d’utiliser l’attribut de **\[ chaîne \]** en même temps que les \[ [premiers attributs \_ is](/windows/desktop/Midl/first-is) \] , \[ [Last \_ is](/windows/desktop/Midl/last-is) \] et \[ [size \_ is](/windows/desktop/Midl/size-is) \] .</span><span class="sxs-lookup"><span data-stu-id="526b6-107">To avoid possible inconsistencies, MIDL does not let you use the **\[string\]** attribute at the same time as the \[ [first\_is](/windows/desktop/Midl/first-is)\], \[ [last\_is](/windows/desktop/Midl/last-is)\], and \[ [size\_is](/windows/desktop/Midl/size-is)\] attributes.</span></span>

<span data-ttu-id="526b6-108">Avec les chaînes terminées par un caractère null en C, vous devez autoriser l’espace pour le caractère null à la fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="526b6-108">With null-terminated strings in C, you must allow space for the null character at the end of the string.</span></span> <span data-ttu-id="526b6-109">Par exemple, lorsque vous déclarez une chaîne qui contient jusqu’à 80 caractères, allouez 81 caractères.</span><span class="sxs-lookup"><span data-stu-id="526b6-109">For example, when declaring a string that will hold up to 80 characters, allocate 81 characters.</span></span> <span data-ttu-id="526b6-110">L’exemple de fichier IDL suivant montre comment déclarer des tableaux avec l’attribut de **\[ chaîne \]** .</span><span class="sxs-lookup"><span data-stu-id="526b6-110">The following sample IDL file demonstrates how to declare arrays with the **\[string\]** attribute.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 