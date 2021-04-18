---
description: Fournit des restrictions pour l’utilisation de valeurs 64 bits dans le cadre d’un chemin d’accès.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Prise en charge des instances de classe pour les valeurs 64 bits
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542960"
---
# <a name="class-instance-support-for-64-bit-values"></a><span data-ttu-id="c7b1e-103">Prise en charge des instances de classe pour les valeurs 64 bits</span><span class="sxs-lookup"><span data-stu-id="c7b1e-103">Class Instance Support for 64-Bit Values</span></span>

<span data-ttu-id="c7b1e-104">Vous pouvez utiliser une valeur de clé 64 bits dans le cadre d’un chemin d’accès, avec les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7b1e-104">You can use a 64-bit key value as part of a path, with the following restrictions:</span></span>

-   <span data-ttu-id="c7b1e-105">Tant que vous ne dépassez pas la plage de 32 bits, vous pouvez assigner et récupérer des valeurs à partir de la clé, comme vous le feriez pour une propriété 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c7b1e-105">As long as you do not exceed the 32-bit range, you can assign and retrieve values from the key as you would a 32-bit property.</span></span>
-   <span data-ttu-id="c7b1e-106">Une fois que vous avez dépassé la valeur entière de 0x7FFFFFFF (pour les types signés), 0x80000000 (pour les types non signés) ou 32 bits, vous devez utiliser des guillemets.</span><span class="sxs-lookup"><span data-stu-id="c7b1e-106">After you exceed the integer value of 0x7FFFFFFF (for signed types), 0x80000000 (for unsigned types), or 32 bits, you must use quotation marks.</span></span>
-   <span data-ttu-id="c7b1e-107">Le seul chemin d’accès valide pour une valeur 64 bits se trouve dans les propriétés **\_ \_ RelPath** ou **\_ \_ path** de l’instance.</span><span class="sxs-lookup"><span data-stu-id="c7b1e-107">The only valid path for a 64-bit value is located in the **\_\_RELPATH** or **\_\_PATH** properties of the instance.</span></span> <span data-ttu-id="c7b1e-108">Par conséquent, WMI ne prend pas en charge la notation hexadécimale pour la valeur équivalente.</span><span class="sxs-lookup"><span data-stu-id="c7b1e-108">As such, WMI does not support the hexadecimal notation for the equivalent value.</span></span>
-   <span data-ttu-id="c7b1e-109">Si WMI enregistre la clé d’instance sous la forme d’un nombre négatif, vous devez utiliser le numéro d’origine pour récupérer l’instance.</span><span class="sxs-lookup"><span data-stu-id="c7b1e-109">If WMI records the instance key as a negative number, then you must use the original number to retrieve the instance.</span></span>

<span data-ttu-id="c7b1e-110">La sémantique de requête n’est pas affectée et se comporte comme prévu.</span><span class="sxs-lookup"><span data-stu-id="c7b1e-110">Query semantics are unaffected and behave as expected.</span></span> <span data-ttu-id="c7b1e-111">Ce comportement affecte uniquement le chemin d’accès de l’objet, les opérations [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)et [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="c7b1e-111">This behavior only affects the object path, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) operations.</span></span>

<span data-ttu-id="c7b1e-112">L’exemple suivant montre que les instances de classe peuvent avoir des valeurs de clé de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c7b1e-112">The following example shows that class instances can have 64-bit key values.</span></span>

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



