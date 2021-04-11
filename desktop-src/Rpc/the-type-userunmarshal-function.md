---
title: Fonction type_UserUnmarshal
description: La \_ fonction de type UserUnmarshal est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031815"
---
# <a name="the-type_userunmarshal-function"></a><span data-ttu-id="921c2-104">Type \_ UserUnmarshal (fonction)</span><span class="sxs-lookup"><span data-stu-id="921c2-104">The type\_UserUnmarshal Function</span></span>

<span data-ttu-id="921c2-105">La fonction **<type> \_ UserUnmarshal** est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [utilisateur \_](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="921c2-105">The **<type>\_UserUnmarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="921c2-106">Les stubs appellent cette fonction pour démarshaler des données côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="921c2-106">The stubs call this function to unmarshal data on the client or server side.</span></span> <span data-ttu-id="921c2-107">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="921c2-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="921c2-108">Le <type> dans le nom de fonction correspond au type utilisateur spécifié dans la définition de type de marshaling de **\[ \_ \] câble** ou d' **\[ utilisateur \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="921c2-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="921c2-109">Ce type peut être non transmissible ou même, lorsqu’il est utilisé avec l’attribut de **\[ \_ Marshal \] utilisateur** , inconnu du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="921c2-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—unknown to the MIDL compiler.</span></span> <span data-ttu-id="921c2-110">Le nom du type de câble (le nom du type transmissible) n’est pas utilisé dans le prototype de la fonction.</span><span class="sxs-lookup"><span data-stu-id="921c2-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="921c2-111">Notez, toutefois, que le type de câble définit la disposition filaire pour les données, comme spécifié par l’ETCD OSF.</span><span class="sxs-lookup"><span data-stu-id="921c2-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="921c2-112">Le paramètre *pFlags* est un pointeur vers un champ d’indicateur **long non signé** .</span><span class="sxs-lookup"><span data-stu-id="921c2-112">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="921c2-113">Le mot supérieur de l’indicateur contient des indicateurs de représentation de données NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère.</span><span class="sxs-lookup"><span data-stu-id="921c2-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="921c2-114">Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM.</span><span class="sxs-lookup"><span data-stu-id="921c2-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="921c2-115">La disposition exacte des indicateurs dans le champ est décrite dans [la fonction type d' \_ utilisateur](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="921c2-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="921c2-116">Le paramètre *pbuffer* est le pointeur de la mémoire tampon en cours.</span><span class="sxs-lookup"><span data-stu-id="921c2-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="921c2-117">Ce pointeur peut être ou ne pas être aligné sur l’entrée.</span><span class="sxs-lookup"><span data-stu-id="921c2-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="921c2-118">Votre fonction **<type> \_ UserUnmarshal** doit aligner le pointeur de la mémoire tampon correctement, démarshaler les données et retourner la nouvelle position de mémoire tampon, qui est l’adresse du premier octet après l’objet non marshalé.</span><span class="sxs-lookup"><span data-stu-id="921c2-118">Your **<type>\_UserUnmarshal** function should align the buffer pointer appropriately, unmarshal the data, and return the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="921c2-119">Le paramètre *pMyObj* est un pointeur vers un objet de type défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="921c2-119">The *pMyObj* parameter is a pointer to a user-defined type object.</span></span>

<span data-ttu-id="921c2-120">Dans un environnement hétérogène, le moteur de NDR effectue toute conversion de données nécessaire avant d’appeler la fonction **<type> \_ UserUnmarshal** .</span><span class="sxs-lookup"><span data-stu-id="921c2-120">In a heterogeneous environment, the NDR engine performs any data conversion necessary before calling the **<type>\_UserUnmarshal** function.</span></span> <span data-ttu-id="921c2-121">Notez que le moteur de NDR effectue cette conversion de données en fonction de la définition de type de câble fournie pour ce type de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="921c2-121">Note that the NDR engine carries out this data conversion according to the wire-type definition supplied for this user data type.</span></span> <span data-ttu-id="921c2-122">L’indicateur indique la représentation des données de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="921c2-122">The flag indicates the data representation of the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="921c2-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="921c2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="921c2-124">Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="921c2-124">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="921c2-125">Marshal de câble \_</span><span class="sxs-lookup"><span data-stu-id="921c2-125">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="921c2-126">Marshal d’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="921c2-126">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 