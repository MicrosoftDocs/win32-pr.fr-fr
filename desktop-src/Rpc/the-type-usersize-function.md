---
title: Fonction type_UserSize
description: La \_ fonction type d’utilisateur est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730020"
---
# <a name="the-type_usersize-function"></a><span data-ttu-id="5152d-104">La fonction type d' \_ utilisateur</span><span class="sxs-lookup"><span data-stu-id="5152d-104">The type\_UserSize Function</span></span>

<span data-ttu-id="5152d-105">La fonction **<type> \_ Users** est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [ \_ utilisateur](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="5152d-105">The **<type>\_UserSize** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="5152d-106">Les stubs appellent cette fonction pour dimensionner la mémoire tampon de données RPC pour l’objet de données utilisateur avant que les données ne soient marshalées côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="5152d-106">The stubs call this function to size the RPC data buffer for the user data object before the data is marshaled on the client or server side.</span></span> <span data-ttu-id="5152d-107">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="5152d-107">The function is defined as:</span></span>

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<span data-ttu-id="5152d-108">Le <type> dans le nom de la fonction signifie User-type, comme spécifié dans la définition de type de marshaling de **\[ \_ \] câble** ou d' **\[ utilisateur \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="5152d-108">The <type> in the function name means the userm-type, as specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="5152d-109">Ce type peut être non transmissible ou même, lorsqu’il est utilisé avec l’attribut de **\[ \_ Marshal \] utilisateur** , inconnu du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="5152d-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute— unknown to the MIDL compiler.</span></span> <span data-ttu-id="5152d-110">Le nom du type de câble (le nom du type transmis sur le réseau) n’est pas utilisé dans le prototype de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5152d-110">The wire type name (the name of the type transmitted across the network) is not used in the function prototype.</span></span> <span data-ttu-id="5152d-111">Notez, toutefois, que le type de câble définit la disposition des données comme spécifié par l’ETCD OSF.</span><span class="sxs-lookup"><span data-stu-id="5152d-111">Note, however, that the wire type defines the layout for the data as specified by OSF DCE.</span></span> <span data-ttu-id="5152d-112">Toutes les données doivent être converties au format de représentation de données réseau (NDR).</span><span class="sxs-lookup"><span data-stu-id="5152d-112">All data must be converted to network data representation (NDR) format.</span></span>

<span data-ttu-id="5152d-113">Le paramètre *pFlags* est un pointeur vers un champ d’indicateur **long non signé** .</span><span class="sxs-lookup"><span data-stu-id="5152d-113">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="5152d-114">Le mot supérieur de l’indicateur contient des indicateurs de format NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère.</span><span class="sxs-lookup"><span data-stu-id="5152d-114">The upper word of the flag contains NDR format flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="5152d-115">Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM.</span><span class="sxs-lookup"><span data-stu-id="5152d-115">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="5152d-116">La disposition exacte des indicateurs dans le champ est indiquée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5152d-116">The exact layout of the flags within the field is shown in the following table.</span></span>



| <span data-ttu-id="5152d-117">Bits</span><span class="sxs-lookup"><span data-stu-id="5152d-117">Bits</span></span>  | <span data-ttu-id="5152d-118">Indicateur</span><span class="sxs-lookup"><span data-stu-id="5152d-118">Flag</span></span>                                  | <span data-ttu-id="5152d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5152d-119">Value</span></span>                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5152d-120">31-24</span><span class="sxs-lookup"><span data-stu-id="5152d-120">31-24</span></span> | <span data-ttu-id="5152d-121">Représentation à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="5152d-121">Floating-point representation</span></span>         | <span data-ttu-id="5152d-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span><span class="sxs-lookup"><span data-stu-id="5152d-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span></span>                                                         |
| <span data-ttu-id="5152d-123">23-20</span><span class="sxs-lookup"><span data-stu-id="5152d-123">23-20</span></span> | <span data-ttu-id="5152d-124">Ordre des octets à virgule flottante et entier</span><span class="sxs-lookup"><span data-stu-id="5152d-124">Integer and floating-point byte order</span></span> | <span data-ttu-id="5152d-125">0 = Big-endian 1 = Little endian</span><span class="sxs-lookup"><span data-stu-id="5152d-125">0 = Big-endian 1 = Little-endian</span></span>                                                          |
| <span data-ttu-id="5152d-126">19-16</span><span class="sxs-lookup"><span data-stu-id="5152d-126">19-16</span></span> | <span data-ttu-id="5152d-127">Représentation de caractères</span><span class="sxs-lookup"><span data-stu-id="5152d-127">Character representation</span></span>              | <span data-ttu-id="5152d-128">0 = ASCII 1 = EBCDIC</span><span class="sxs-lookup"><span data-stu-id="5152d-128">0 = ASCII 1 = EBCDIC</span></span>                                                                      |
| <span data-ttu-id="5152d-129">15-0</span><span class="sxs-lookup"><span data-stu-id="5152d-129">15-0</span></span>  | <span data-ttu-id="5152d-130">Indicateur de contexte de marshaling</span><span class="sxs-lookup"><span data-stu-id="5152d-130">Marshaling context flag</span></span>               | <span data-ttu-id="5152d-131">0 = MSHCTX \_ local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ InProc</span><span class="sxs-lookup"><span data-stu-id="5152d-131">0 = MSHCTX\_LOCAL 1 = MSHCTX\_NOSHAREDMEM 2 = MSHCTX\_DIFFERENTMACHINE 3 = MSHCTX\_INPROC</span></span> |



 

<span data-ttu-id="5152d-132">L’indicateur de contexte de marshaling permet de modifier le comportement de votre routine en fonction du contexte de l’appel RPC.</span><span class="sxs-lookup"><span data-stu-id="5152d-132">The marshaling context flag makes it possible to alter the behavior of your routine depending on the context for the RPC call.</span></span> <span data-ttu-id="5152d-133">Par exemple, si vous avez un handle (**long**) vers un bloc de données, vous pouvez envoyer le descripteur pour un appel in-process, mais vous enverrez les données réelles pour un appel à un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5152d-133">For example, if you have a handle (**long**) to a block of data, you could send the handle for an in-process call, but you would send the actual data for a call to a different machine.</span></span> <span data-ttu-id="5152d-134">L’indicateur de contexte de marshaling et ses valeurs sont définis dans les fichiers Wtypes. h et Wtypes. idl dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="5152d-134">The marshaling context flag and its values are defined in the Wtypes.h and Wtypes.idl files in the Platform Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="5152d-135">Lorsque le type de câble est correctement défini, il n’est pas nécessaire d’utiliser les indicateurs de format NDR, car le moteur de NDR effectue les conversions nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5152d-135">When the wire type is properly defined, you do not have to use the NDR format flags, as the NDR engine performs the necessary conversions.</span></span>

 

<span data-ttu-id="5152d-136">Le *StartingSize* un paramètre est l’offset de la mémoire tampon actuelle.</span><span class="sxs-lookup"><span data-stu-id="5152d-136">The *StartingSize* a parameter is the current buffer offset.</span></span> <span data-ttu-id="5152d-137">La taille de départ indique l’offset de la mémoire tampon pour l’objet utilisateur, et elle peut ou non être correctement alignée.</span><span class="sxs-lookup"><span data-stu-id="5152d-137">The starting size indicates the buffer offset for the user object, and it may or may not be aligned properly.</span></span> <span data-ttu-id="5152d-138">Votre routine doit tenir compte de ce qui est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5152d-138">Your routine should account for whatever padding is necessary.</span></span>

<span data-ttu-id="5152d-139">Le paramètre *pMyObj* est un pointeur vers un objet de type utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5152d-139">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="5152d-140">La valeur de retour est la nouvelle position de décalage ou de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5152d-140">The return value is the new offset or buffer position.</span></span> <span data-ttu-id="5152d-141">La fonction doit retourner la taille cumulée, qui correspond à la taille de départ et au remplissage possible plus la taille des données.</span><span class="sxs-lookup"><span data-stu-id="5152d-141">The function should return the cumulative size, which is the starting size plus possible padding plus the data size.</span></span>

<span data-ttu-id="5152d-142">La fonction **<type> \_ Users** peut retourner un surestime de la taille nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5152d-142">The **<type>\_UserSize** function can return an overestimate of the size needed.</span></span> <span data-ttu-id="5152d-143">La taille réelle de la mémoire tampon envoyée est définie par la taille des données, et non par la taille d’allocation de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5152d-143">The actual size of the sent buffer is defined by the data size, not by the buffer allocation size.</span></span>

<span data-ttu-id="5152d-144">La fonction **<type> \_ utilisateur** n’est pas appelée si la taille du câble peut être calculée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="5152d-144">The **<type>\_UserSize** function is not called if the wire size can be computed at compile time.</span></span> <span data-ttu-id="5152d-145">Notez que pour la plupart des unions, même s’il n’y a pas de pointeurs, la taille réelle de la représentation de câble ne peut être déterminée qu’au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5152d-145">Note that for most unions, even if there are no pointers, the actual size of the wire representation can be determined only at run time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5152d-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5152d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5152d-147">Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="5152d-147">Marshaling rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="5152d-148">Marshal d’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="5152d-148">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="5152d-149">Marshal de câble \_</span><span class="sxs-lookup"><span data-stu-id="5152d-149">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 