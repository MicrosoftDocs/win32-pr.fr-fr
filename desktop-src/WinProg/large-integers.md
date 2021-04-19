---
title: Entiers volumineux
description: Les grandes fonctions et structures entières offraient à l’origine une prise en charge des valeurs 64 bits sur Windows 32 bits.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- entiers volumineux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513545"
---
# <a name="large-integers"></a><span data-ttu-id="a80ce-104">Entiers volumineux</span><span class="sxs-lookup"><span data-stu-id="a80ce-104">Large Integers</span></span>

<span data-ttu-id="a80ce-105">Les grandes fonctions et structures entières offraient à l’origine une prise en charge des valeurs 64 bits sur Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a80ce-105">The large integer functions and structures originally provided support for 64-bit values on 32-bit Windows.</span></span> <span data-ttu-id="a80ce-106">Désormais, votre compilateur C peut prendre en charge les entiers 64 bits en mode natif.</span><span class="sxs-lookup"><span data-stu-id="a80ce-106">Now, your C compiler may support 64-bit integers natively.</span></span> <span data-ttu-id="a80ce-107">Par exemple, Microsoft Visual C++ prend en charge le type d’entier de taille [**\_ \_ Int64**](/windows/desktop/Midl/--int64) .</span><span class="sxs-lookup"><span data-stu-id="a80ce-107">For example, Microsoft Visual C++ supports the [**\_\_int64**](/windows/desktop/Midl/--int64) sized integer type.</span></span> <span data-ttu-id="a80ce-108">Pour plus d’informations, consultez la documentation fournie avec votre compilateur C.</span><span class="sxs-lookup"><span data-stu-id="a80ce-108">For more information, see the documentation included with your C compiler.</span></span>

<span data-ttu-id="a80ce-109">Pour plus d’informations sur les entiers 64 bits sous Windows 64 bits, consultez [nouveaux types de données](/windows/desktop/WinProg64/the-new-data-types).</span><span class="sxs-lookup"><span data-stu-id="a80ce-109">For information on 64-bit integers on 64-bit Windows, see [The New Data Types](/windows/desktop/WinProg64/the-new-data-types).</span></span>

## <a name="large-integer-operations"></a><span data-ttu-id="a80ce-110">Opérations sur les entiers volumineux</span><span class="sxs-lookup"><span data-stu-id="a80ce-110">Large Integer Operations</span></span>

<span data-ttu-id="a80ce-111">Les applications peuvent multiplier des entiers 32 bits signés ou non signés, générant des résultats 64 bits, à l’aide des fonctions [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) et [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="a80ce-111">Applications can multiply signed or unsigned 32-bit integers, generating 64-bit results, by using the [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) and [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) functions.</span></span> <span data-ttu-id="a80ce-112">Les applications peuvent décaler les bits des valeurs 64 bits vers la gauche ou vers la droite à l’aide des fonctions [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)et [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) .</span><span class="sxs-lookup"><span data-stu-id="a80ce-112">Applications can shift bits in 64-bit values to the left or right by using the [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32), and [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) functions.</span></span> <span data-ttu-id="a80ce-113">Ces fonctions fournissent des décalages logiques et arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="a80ce-113">These functions provide logical and arithmetic shifting.</span></span>

<span data-ttu-id="a80ce-114">Les applications peuvent également multiplier et diviser des valeurs 32 bits en une seule opération à l’aide de la fonction [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) .</span><span class="sxs-lookup"><span data-stu-id="a80ce-114">Applications can also multiply and divide 32-bit values in a single operation by using the [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) function.</span></span> <span data-ttu-id="a80ce-115">Bien que le résultat de l’opération soit une valeur 32 bits, la fonction stocke le résultat intermédiaire sous la forme d’une valeur 64 bits, de sorte que les informations ne sont pas perdues lorsque de grandes valeurs 32 bits sont multipliées et divisées.</span><span class="sxs-lookup"><span data-stu-id="a80ce-115">Although the result of the operation is a 32-bit value, the function stores the intermediate result as a 64-bit value, so that information is not lost when large 32-bit values are multiplied and divided.</span></span>

## <a name="large-integer-reference"></a><span data-ttu-id="a80ce-116">Référence d’entier long</span><span class="sxs-lookup"><span data-stu-id="a80ce-116">Large Integer Reference</span></span>

-   [<span data-ttu-id="a80ce-117">Fonctions entières de type long</span><span class="sxs-lookup"><span data-stu-id="a80ce-117">Large Integer Functions</span></span>](large-integer-functions.md)
-   [<span data-ttu-id="a80ce-118">Structures d’entiers longs</span><span class="sxs-lookup"><span data-stu-id="a80ce-118">Large Integer Structures</span></span>](large-integer-structures.md)

 

 