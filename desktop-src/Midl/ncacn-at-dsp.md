---
title: attribut ncacn_at_dsp
description: Le \_ \_ mot clé ncacn at DSP identifie le DSP AppleTalk comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940953"
---
# <a name="ncacn_at_dsp-attribute"></a><span data-ttu-id="ba19d-105">ncacn \_ au niveau de l' \_ attribut DSP</span><span class="sxs-lookup"><span data-stu-id="ba19d-105">ncacn\_at\_dsp attribute</span></span>

<span data-ttu-id="ba19d-106">Le mot clé **ncacn \_ at \_ DSP** identifie le DSP AppleTalk comme famille de protocoles pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ba19d-106">The **ncacn\_at\_dsp** keyword identifies AppleTalk DSP as the protocol family for the endpoint.</span></span> <span data-ttu-id="ba19d-107">Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="ba19d-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="ba19d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba19d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba19d-109">*nom du port*</span><span class="sxs-lookup"><span data-stu-id="ba19d-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ba19d-110">Spécifie une chaîne de caractères d’une longueur maximale de 22 octets.</span><span class="sxs-lookup"><span data-stu-id="ba19d-110">Specifies a character string up to 22 bytes long.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba19d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ba19d-111">Remarks</span></span>

<span data-ttu-id="ba19d-112">La syntaxe de la chaîne de port DSP AppleTalk, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL.</span><span class="sxs-lookup"><span data-stu-id="ba19d-112">The syntax of the AppleTalk DSP port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="ba19d-113">Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte.</span><span class="sxs-lookup"><span data-stu-id="ba19d-113">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="ba19d-114">Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="ba19d-114">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="ba19d-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="ba19d-115">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="ba19d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba19d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba19d-117">**poste**</span><span class="sxs-lookup"><span data-stu-id="ba19d-117">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="ba19d-118">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="ba19d-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ba19d-119">**liaison de chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba19d-119">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 