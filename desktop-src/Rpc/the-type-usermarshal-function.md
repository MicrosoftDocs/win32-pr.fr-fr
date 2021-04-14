---
title: Fonction type_UserMarshal
description: La \_ fonction de type UserMarshal est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382784"
---
# <a name="the-type_usermarshal-function"></a><span data-ttu-id="b999c-104">Type \_ UserMarshal (fonction)</span><span class="sxs-lookup"><span data-stu-id="b999c-104">The type\_UserMarshal Function</span></span>

<span data-ttu-id="b999c-105">La fonction **<type> \_ UserMarshal** est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [utilisateur \_](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="b999c-105">The **<type>\_UserMarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="b999c-106">Les stubs appellent cette fonction pour marshaler des données côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="b999c-106">The stubs call this function to marshal data on the client or server side.</span></span> <span data-ttu-id="b999c-107">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="b999c-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="b999c-108">Le <type> dans le nom de fonction correspond au type utilisateur spécifié dans la définition de type de marshaling de **\[ \_ \] câble** ou d' **\[ utilisateur \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="b999c-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="b999c-109">Ce type peut être non transmissible ou même, lorsqu’il est utilisé avec l’attribut **\[ User \_ Marshal \]** (un type inconnu pour le compilateur MIDL).</span><span class="sxs-lookup"><span data-stu-id="b999c-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—a type unknown to the MIDL compiler.</span></span> <span data-ttu-id="b999c-110">Le nom du type de câble (le nom du type transmissible) n’est pas utilisé dans le prototype de la fonction.</span><span class="sxs-lookup"><span data-stu-id="b999c-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="b999c-111">Notez, toutefois, que le type de câble définit la disposition filaire pour les données, comme spécifié par l’ETCD OSF.</span><span class="sxs-lookup"><span data-stu-id="b999c-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="b999c-112">Le paramètre *pFlags* est un pointeur vers un champ d’indicateur long non signé.</span><span class="sxs-lookup"><span data-stu-id="b999c-112">The *pFlags* parameter is a pointer to an unsigned long flag field.</span></span> <span data-ttu-id="b999c-113">Le mot supérieur de l’indicateur contient des indicateurs de représentation de données NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère.</span><span class="sxs-lookup"><span data-stu-id="b999c-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="b999c-114">Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM.</span><span class="sxs-lookup"><span data-stu-id="b999c-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="b999c-115">La disposition exacte des indicateurs dans le champ est décrite dans [la fonction type d' \_ utilisateur](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="b999c-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="b999c-116">Le paramètre *pbuffer* est le pointeur de la mémoire tampon en cours.</span><span class="sxs-lookup"><span data-stu-id="b999c-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="b999c-117">Ce pointeur peut être ou ne pas être aligné sur l’entrée.</span><span class="sxs-lookup"><span data-stu-id="b999c-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="b999c-118">Votre fonction **<type> \_ UserMarshal** doit aligner le pointeur de la mémoire tampon correctement, marshaler les données et retourner la nouvelle position de mémoire tampon, qui est l’adresse du premier octet après l’objet marshalé.</span><span class="sxs-lookup"><span data-stu-id="b999c-118">Your **<type>\_UserMarshal** function should align the buffer pointer appropriately, marshal the data, and return the new buffer position, which is the address of the first byte after the marshaled object.</span></span> <span data-ttu-id="b999c-119">Gardez à l’esprit que la spécification de type de câble détermine la disposition réelle des données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b999c-119">Keep in mind that the wire type specification determines the actual layout of the data in the buffer.</span></span>

<span data-ttu-id="b999c-120">Le paramètre *pMyObj* est un pointeur vers un objet de type utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b999c-120">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="b999c-121">La valeur de retour est la nouvelle position de mémoire tampon, qui est l’adresse du premier octet après l’objet non marshalé.</span><span class="sxs-lookup"><span data-stu-id="b999c-121">The return value is the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="b999c-122">Un dépassement de capacité de la mémoire tampon peut se produire lorsque vous calculez de manière incorrecte la taille des données et essayez de marshaler plus de données que prévu.</span><span class="sxs-lookup"><span data-stu-id="b999c-122">Buffer overflow can occur when you incorrectly calculate the size of the data and attempt to marshal more data than expected.</span></span> <span data-ttu-id="b999c-123">Veillez à éviter cette situation.</span><span class="sxs-lookup"><span data-stu-id="b999c-123">You should be careful to avoid this situation.</span></span> <span data-ttu-id="b999c-124">Vous pouvez le vérifier à l’aide du pointeur retourné par **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="b999c-124">You can check against it by using the pointer that **<type>\_UserMarshal** returns.</span></span> <span data-ttu-id="b999c-125">Dans le cas contraire, vous risquez que le moteur de NDR génère une exception de dépassement de mémoire tampon plus tard.</span><span class="sxs-lookup"><span data-stu-id="b999c-125">Otherwise, you risk having the NDR engine raise a buffer-overflow exception later.</span></span>

<span data-ttu-id="b999c-126">Les exceptions doivent être interceptées et gérées localement, les exceptions ne doivent pas être autorisées à propigated la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="b999c-126">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b999c-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b999c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b999c-128">Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="b999c-128">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="b999c-129">Marshal de câble \_</span><span class="sxs-lookup"><span data-stu-id="b999c-129">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="b999c-130">Marshal d’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="b999c-130">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 