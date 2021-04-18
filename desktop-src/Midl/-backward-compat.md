---
title: Commutateur/backward_compat
description: Le \_ commutateur de compatibilité/Backward indique au compilateur MIDL de désactiver certaines fonctionnalités avancées lors de la génération de stubs RPC/com.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106529052"
---
# <a name="backward_compat-switch"></a><span data-ttu-id="e1f9f-103">\_commutateur de compatibilité/Backward</span><span class="sxs-lookup"><span data-stu-id="e1f9f-103">/backward\_compat Switch</span></span>

<span data-ttu-id="e1f9f-104">Le \_ commutateur de compatibilité/Backward indique au compilateur MIDL de désactiver certaines fonctionnalités avancées lors de la génération de stubs RPC/com.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-104">The /backward\_compat switch directs the MIDL compiler to turn off some advanced features when generating RPC/COM stubs.</span></span>

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a><span data-ttu-id="e1f9f-105">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="e1f9f-105">Switch Options</span></span>

<span data-ttu-id="e1f9f-106">*taille de MAYBENULL \_*</span><span class="sxs-lookup"><span data-stu-id="e1f9f-106">*maybenull\_sizeis*</span></span><dl> <span data-ttu-id="e1f9f-107">Applique l’attribut de [ \[ désactivation de la \_ \_ \] vérification de cohérence](disable-consistence-check.md) à une compilation MIDL entière.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-107">Applies the [\[disable\_consistency\_check\]](disable-consistence-check.md) attribute to an entire MIDL compilation.</span></span>  
</dl>

<span data-ttu-id="e1f9f-108">*zeroout \_ alignmentgap*</span><span class="sxs-lookup"><span data-stu-id="e1f9f-108">*zeroout\_alignmentgap*</span></span><dl> <span data-ttu-id="e1f9f-109">Désactive les écarts de zéro dans la mémoire tampon marshalée.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-109">Turns off zeroing out gaps in the marshaled buffer.</span></span>  
</dl>

<span data-ttu-id="e1f9f-110">*Séquence \_ d' \_ échappement ByValue BSTR*</span><span class="sxs-lookup"><span data-stu-id="e1f9f-110">*BSTR\_byvalue\_escaping*</span></span><dl> <span data-ttu-id="e1f9f-111">Indique au compilateur MIDL d’honorer les séquences d’échappement, telles que â € ̃ \\ nâ,™ ou â € ̃ \\ t €™ in BSTR.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-111">Directs the MIDL compiler to honor escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in BSTRs.</span></span>  
</dl>

<span data-ttu-id="e1f9f-112">*DefaultValue de chaîne \_*</span><span class="sxs-lookup"><span data-stu-id="e1f9f-112">*string\_defaultvalue*</span></span><dl> <span data-ttu-id="e1f9f-113">Force le compilateur MIDL à contraindre les chaînes des attributs [**\[ DEFAULTVALUE \]**](defaultvalue.md) en variant. \_Type VT I4 avant de convertir la valeur en type correct.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-113">Forces the MIDL compiler to coerce strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span>  
</dl>

<span data-ttu-id="e1f9f-114">*\_WCHAR \_ t signé*</span><span class="sxs-lookup"><span data-stu-id="e1f9f-114">*signed\_wchar\_t*</span></span><dl> <span data-ttu-id="e1f9f-115">Dirige MIDL pour traiter le type WCHAR \_ t comme signé pour la compatibilité avec Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-115">Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>  
</dl>

## <a name="remarks"></a><span data-ttu-id="e1f9f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e1f9f-116">Remarks</span></span>

-   <span data-ttu-id="e1f9f-117">*\_ taille de MAYBENULL*: voir \[ désactiver \_ la \_ vérification de cohérence \] .</span><span class="sxs-lookup"><span data-stu-id="e1f9f-117">*maybenull\_sizeis*: See \[disable\_consistency\_check\].</span></span>
-   <span data-ttu-id="e1f9f-118">*zeroout \_ alignmentgap*: lorsque IDLs sont compilés avec â € «Target nt60 ou version ultérieure, MIDL crée des stubs qui éliminent les éventuels écarts d’alignement entre les membres ou une structure dans la mémoire tampon de câble.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-118">*zeroout\_alignmentgap*: When IDLs are compiled with â€“target NT60 or higher, MIDL will create stubs that zero out any alignment gaps between members or a structure in the wire buffer.</span></span> <span data-ttu-id="e1f9f-119">Le commutateur de ligne de commande */Backward \_ compat zeroout \_ alignmentgap* dirige MIDL pour désactiver cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-119">The command line switch */backward\_compat zeroout\_alignmentgap* directs MIDL to disable this feature.</span></span>

    <span data-ttu-id="e1f9f-120">Dans l’exemple de structure suivant, la mémoire tampon de câble contient un intervalle d’alignement de 7 octets pour aligner le membre hyper sur 8 après le membre char.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-120">In the following example structure, the wire buffer contains a 7 byte alignment gap to align the hyper member to 8 after the char member.</span></span> <span data-ttu-id="e1f9f-121">Avec â € «Target NT60 ou version ultérieure, MIDL aura zéro ce fossé, sauf si le commutateur est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-121">With â€“target NT60 or higher, MIDL will zero out that gap unless the switch is used.</span></span>

    <span data-ttu-id="e1f9f-122">Fichier IDL :</span><span class="sxs-lookup"><span data-stu-id="e1f9f-122">IDL file:</span></span>

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    <span data-ttu-id="e1f9f-123">Ce commutateur peut apporter une légère amélioration des performances avec des augmentations potentiellement significatives du risque de divulgation.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-123">This switch can provide a slight performance improvement with potentially significant increases in disclosure risk.</span></span>

-   <span data-ttu-id="e1f9f-124">Type d' *\_ \_ échappement BSTR ByValue*: par défaut, le compilateur MIDL ne traite pas les séquences d’échappement telles que â € ̃ \\ nâ,™ ou â € ̃ \\ ™ t dans les constantes de chaîne pour OLE Automation lors de la conversion d’une constante de chaîne en types VT \_ LPSTR ou VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-124">*BSTR\_byvalue\_escaping*: By default, the MIDL compiler does not process escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in string constants for OLE Automation when converting a string constant to types VT\_LPSTR or VT\_LPWSTR.</span></span> <span data-ttu-id="e1f9f-125">Avec cette option de commutateur de compatibilité descendante, les séquences d’échappement sont évaluées.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-125">With this backward compatibility switch option, the escape sequences are evaluated.</span></span>
-   <span data-ttu-id="e1f9f-126">*String \_ DefaultValue*: force le compilateur MIDL à contraindre les chaînes numériques des attributs [**\[ \] DefaultValue**](defaultvalue.md) en variant. \_Type VT I4 avant de convertir la valeur en type correct.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-126">*string\_defaultvalue*: Forces the MIDL compiler to coerce numeric strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span> <span data-ttu-id="e1f9f-127">Cela peut entraîner une perte de précision dans certains cas. par conséquent, cette option de commutation n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-127">This can lead to loss of precision in some cases, so this switch option is not recommended.</span></span>
-   <span data-ttu-id="e1f9f-128">*\_ WCHAR \_ t signé*: demande à MIDL de traiter le \_ type WCHAR t comme signé pour la compatibilité avec Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e1f9f-128">*signed\_wchar\_t*: Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>

 

 




