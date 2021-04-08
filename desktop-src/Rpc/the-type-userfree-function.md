---
title: Fonction type_UserFree
description: La \_ fonction de type UserFree est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727444"
---
# <a name="the-type_userfree-function"></a><span data-ttu-id="22090-104">Type \_ UserFree (fonction)</span><span class="sxs-lookup"><span data-stu-id="22090-104">The type\_UserFree Function</span></span>

<span data-ttu-id="22090-105">La fonction **<type> \_ UserFree** est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [utilisateur \_](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="22090-105">The **<type>\_UserFree** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="22090-106">Les stubs appellent cette fonction pour libérer les données côté serveur.</span><span class="sxs-lookup"><span data-stu-id="22090-106">The stubs call this function to free the data on the server side.</span></span> <span data-ttu-id="22090-107">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="22090-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<span data-ttu-id="22090-108">Le <type> dans le nom de fonction correspond au type utilisateur spécifié dans la définition de type de marshaling de **\[ \_ \] câble** ou d' **\[ utilisateur \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="22090-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span>

<span data-ttu-id="22090-109">Le paramètre *pFlags* est un pointeur vers un champ d’indicateur **long non signé** .</span><span class="sxs-lookup"><span data-stu-id="22090-109">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="22090-110">Le mot supérieur de l’indicateur contient des indicateurs de représentation de données NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère.</span><span class="sxs-lookup"><span data-stu-id="22090-110">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="22090-111">Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM.</span><span class="sxs-lookup"><span data-stu-id="22090-111">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="22090-112">La disposition exacte des indicateurs dans le champ est décrite dans [la fonction type d' \_ utilisateur](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="22090-112">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="22090-113">Le paramètre *pMyObj* est un pointeur vers un objet de type utilisateur.</span><span class="sxs-lookup"><span data-stu-id="22090-113">The *pMyObj* parameter is a pointer to a user type object.</span></span> <span data-ttu-id="22090-114">Le moteur de NDR libère l’objet de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="22090-114">The NDR engine frees the top-level object.</span></span> <span data-ttu-id="22090-115">Vous êtes responsable de la libération des objets sur lesquels l’objet de niveau supérieur peut pointer.</span><span class="sxs-lookup"><span data-stu-id="22090-115">You are responsible for freeing any objects to which the top-level object may point.</span></span>

<span data-ttu-id="22090-116">Les exceptions doivent être interceptées et gérées localement, les exceptions ne doivent pas être autorisées à propigated la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="22090-116">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22090-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22090-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22090-118">Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="22090-118">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="22090-119">Marshal de câble \_</span><span class="sxs-lookup"><span data-stu-id="22090-119">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="22090-120">Marshal d’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="22090-120">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 