---
title: Propriété de domaine ITsSbClientConnection
description: Récupère une valeur qui indique le nom de domaine du client Connexion Bureau à distance (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété de domaine
- Services Bureau à distance de propriété de domaine, interface ITsSbClientConnection
- Services Bureau à distance de l’interface ITsSbClientConnection, propriété de domaine
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532054"
---
# <a name="itssbclientconnectiondomain-property"></a><span data-ttu-id="d79f5-106">ITsSbClientConnection ::D propriété omaine</span><span class="sxs-lookup"><span data-stu-id="d79f5-106">ITsSbClientConnection::Domain property</span></span>

<span data-ttu-id="d79f5-107">Récupère une valeur qui indique le nom de domaine du client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="d79f5-107">Retrieves a value that indicates the domain name of the Remote Desktop Connection (RDC) client.</span></span>

<span data-ttu-id="d79f5-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d79f5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d79f5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d79f5-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="d79f5-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d79f5-110">Property value</span></span>

<span data-ttu-id="d79f5-111">Pointeur vers une variable **BSTR** qui contient le nom de domaine du client RDC.</span><span class="sxs-lookup"><span data-stu-id="d79f5-111">A pointer to a **BSTR** variable that contains the domain name of the RDC client.</span></span> <span data-ttu-id="d79f5-112">Lorsque vous avez fini d’utiliser la chaîne, libérez-la en appelant la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="d79f5-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d79f5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d79f5-113">Requirements</span></span>



| <span data-ttu-id="d79f5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d79f5-114">Requirement</span></span> | <span data-ttu-id="d79f5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d79f5-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d79f5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d79f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d79f5-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d79f5-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d79f5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d79f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d79f5-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d79f5-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d79f5-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="d79f5-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d79f5-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d79f5-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d79f5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d79f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d79f5-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="d79f5-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

