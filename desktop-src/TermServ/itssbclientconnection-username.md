---
title: Propriété du nom d’utilisateur ITsSbClientConnection
description: Récupère une valeur qui indique le nom de l’utilisateur qui a initié la connexion.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Propriété UserName Services Bureau à distance
- Propriété UserName Services Bureau à distance, interface ITsSbClientConnection
- Services Bureau à distance de l’interface ITsSbClientConnection, propriété UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317434"
---
# <a name="itssbclientconnectionusername-property"></a><span data-ttu-id="e340b-106">ITsSbClientConnection :: UserName, propriété</span><span class="sxs-lookup"><span data-stu-id="e340b-106">ITsSbClientConnection::UserName property</span></span>

<span data-ttu-id="e340b-107">Récupère une valeur qui indique le nom de l’utilisateur qui a initié la connexion.</span><span class="sxs-lookup"><span data-stu-id="e340b-107">Retrieves a value that indicates the name of the user who initiated the connection.</span></span>

<span data-ttu-id="e340b-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e340b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e340b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e340b-109">Syntax</span></span>


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="e340b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e340b-110">Property value</span></span>

<span data-ttu-id="e340b-111">Pointeur vers un nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e340b-111">A pointer to a user name.</span></span> <span data-ttu-id="e340b-112">Lorsque vous avez fini d’utiliser la chaîne, libérez-la en appelant la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="e340b-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e340b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e340b-113">Requirements</span></span>



| <span data-ttu-id="e340b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e340b-114">Requirement</span></span> | <span data-ttu-id="e340b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e340b-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e340b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e340b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e340b-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e340b-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e340b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e340b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e340b-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e340b-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e340b-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="e340b-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e340b-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e340b-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e340b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e340b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e340b-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e340b-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

