---
title: Règles de marshaling pour user_marshal et wire_marshal
description: La spécification OSF-DCE pour le marshaling des types de pointeurs incorporés exige que vous observiez les restrictions suivantes lors de l’implémentation des fonctions type d' \_ utilisateur, type \_ UserMarshal et type \_ UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728860"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a><span data-ttu-id="f76bf-103">Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="f76bf-103">Marshaling Rules for user\_marshal and wire\_marshal</span></span>

<span data-ttu-id="f76bf-104">La spécification OSF-DCE pour le marshaling des types de pointeurs incorporés exige que vous observiez les restrictions suivantes lors de l’implémentation des <type> \_ fonctions utilisateur, <type> \_ UserMarshal et <type> \_ UserUnMarshal.</span><span class="sxs-lookup"><span data-stu-id="f76bf-104">The OSF-DCE specification for marshaling embedded pointer types requires that you observe the following restrictions when implementing the <type>\_UserSize, <type>\_UserMarshal, and <type>\_UserUnMarshal functions.</span></span> <span data-ttu-id="f76bf-105">(Les règles et les exemples fournis ici sont pour le marshaling.</span><span class="sxs-lookup"><span data-stu-id="f76bf-105">(The rules and examples given here are for marshaling.</span></span> <span data-ttu-id="f76bf-106">Toutefois, vos routines de dimensionnement et de démarshaling doivent respecter les mêmes restrictions) :</span><span class="sxs-lookup"><span data-stu-id="f76bf-106">However, your sizing and unmarshaling routines must follow the same restrictions):</span></span>

-   <span data-ttu-id="f76bf-107">Si le type de câble est un type plat sans pointeurs, votre routine de marshaling pour le type utilisateur correspondant doit simplement marshaler les données en fonction de la disposition du type de câble.</span><span class="sxs-lookup"><span data-stu-id="f76bf-107">If the wire-type is a flat type with no pointers, your marshaling routine for the corresponding userm-type should simply marshal the data according to the layout of the wire-type.</span></span> <span data-ttu-id="f76bf-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f76bf-108">For example:</span></span>

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    <span data-ttu-id="f76bf-109">Notez que le type de câble **long** est un type plat.</span><span class="sxs-lookup"><span data-stu-id="f76bf-109">Note that the wire type, **long**, is a flat type.</span></span> <span data-ttu-id="f76bf-110">Le handle de la \_ \_ fonction UserMarshal marshale une **valeur de type long** chaque fois qu’un \_ objet descripteur de handle lui est passé.</span><span class="sxs-lookup"><span data-stu-id="f76bf-110">Your HANDLE\_HANDLE\_UserMarshal function marshals a **long** whenever a HANDLE\_HANDLE object is passed to it.</span></span>

-   <span data-ttu-id="f76bf-111">Si le type de câble est un pointeur vers un autre type, votre routine de marshaling pour le type utilisateur correspondant doit marshaler les données en fonction de la disposition du type vers lequel pointe le type de réseau.</span><span class="sxs-lookup"><span data-stu-id="f76bf-111">If the wire-type is a pointer to another type, your marshaling routine for the corresponding userm-type should marshal the data according to the layout for the type that the wire-type points to.</span></span> <span data-ttu-id="f76bf-112">Le moteur de NDR s’occupe du pointeur.</span><span class="sxs-lookup"><span data-stu-id="f76bf-112">The NDR engine takes care of the pointer.</span></span> <span data-ttu-id="f76bf-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f76bf-113">For example:</span></span>

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    <span data-ttu-id="f76bf-114">Notez que le type de câble **, \_ type de câble**, est un type pointeur.</span><span class="sxs-lookup"><span data-stu-id="f76bf-114">Note that the wire type, **WIRE\_TYPE**, is a pointer type.</span></span> <span data-ttu-id="f76bf-115">Votre fonction de gestion de \_ données \_ UserMarshal marshale les données associées au handle, à l’aide de la disposition HDATA, plutôt que de la \* disposition HDATA.</span><span class="sxs-lookup"><span data-stu-id="f76bf-115">Your HANDLE\_DATA\_UserMarshal function marshals the data related to the handle, using the HDATA layout, rather than the HDATA \* layout.</span></span>

-   <span data-ttu-id="f76bf-116">Un type de câble doit être un type de données plat ou un type pointeur.</span><span class="sxs-lookup"><span data-stu-id="f76bf-116">A wire-type must be either a flat data type or a pointer type.</span></span> <span data-ttu-id="f76bf-117">Si votre type transmissible doit être autre chose (une structure avec des pointeurs, par exemple), utilisez un pointeur vers le type souhaité comme type de câble.</span><span class="sxs-lookup"><span data-stu-id="f76bf-117">If your transmissible type must be something else (a structure with pointers, for example), use a pointer to your desired type as the wire-type.</span></span>

<span data-ttu-id="f76bf-118">L’effet de ces restrictions est que les types définis avec les attributs de marshaling de \[ [**câble \_**](/windows/desktop/Midl/wire-marshal) \] ou d' \[ [**utilisateur \_**](/windows/desktop/Midl/user-marshal) \] peuvent être incorporés librement dans d’autres types.</span><span class="sxs-lookup"><span data-stu-id="f76bf-118">The effect of these restrictions is that the types defined with the \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\] or \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\] attributes can be freely embedded in other types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f76bf-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f76bf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f76bf-120">**Marshal de câble \_**</span><span class="sxs-lookup"><span data-stu-id="f76bf-120">**wire\_marshal**</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="f76bf-121">**Marshal d’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="f76bf-121">**user\_marshal**</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="f76bf-122">La fonction type d' \_ utilisateur</span><span class="sxs-lookup"><span data-stu-id="f76bf-122">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
</dt> <dt>

[<span data-ttu-id="f76bf-123">Type \_ UserMarshal (fonction)</span><span class="sxs-lookup"><span data-stu-id="f76bf-123">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
</dt> <dt>

[<span data-ttu-id="f76bf-124">Thetype \_ UserUnMarshalFunction</span><span class="sxs-lookup"><span data-stu-id="f76bf-124">Thetype\_UserUnMarshalFunction</span></span>](the-type-userunmarshal-function.md)
</dt> <dt>

[<span data-ttu-id="f76bf-125">Thetype \_ UserFreeFunction</span><span class="sxs-lookup"><span data-stu-id="f76bf-125">Thetype\_UserFreeFunction</span></span>](the-type-userfree-function.md)
</dt> </dl>

 

 