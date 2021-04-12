---
title: AccessPermission
description: Décrit la liste de Access Control (ACL) des principaux qui peuvent accéder aux instances de cette classe. Cette liste de contrôle d’accès est utilisée uniquement par les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valeur de Registre AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463738"
---
# <a name="accesspermission"></a><span data-ttu-id="c32bd-105">AccessPermission</span><span class="sxs-lookup"><span data-stu-id="c32bd-105">AccessPermission</span></span>

<span data-ttu-id="c32bd-106">Décrit la liste de Access Control (ACL) des principaux qui peuvent accéder aux instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="c32bd-106">Describes the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="c32bd-107">Cette liste de contrôle d’accès est utilisée uniquement par les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c32bd-107">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c32bd-108">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="c32bd-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="c32bd-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c32bd-109">Remarks</span></span>

<span data-ttu-id="c32bd-110">Il s’agit d’une valeur **\_ binaire de Reg** .</span><span class="sxs-lookup"><span data-stu-id="c32bd-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="c32bd-111">Il contient des données décrivant la liste de Access Control (ACL) des principaux qui peuvent accéder aux instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="c32bd-111">It contains data describing the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="c32bd-112">Lors de la réception d’une demande de connexion à un objet existant de cette classe, la liste de contrôle d’accès est vérifiée par l’application appelée en usurpant l’identité de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c32bd-112">Upon receiving a request to connect to an existing object of this class, the ACL is checked by the application being called while impersonating the caller.</span></span> <span data-ttu-id="c32bd-113">Si la vérification de l’accès échoue, la connexion n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="c32bd-113">If the access-check fails, the connection is disallowed.</span></span> <span data-ttu-id="c32bd-114">Si cette valeur nommée n’existe pas, la liste de contrôle d’accès [**DefaultAccessPermission**](defaultaccesspermission.md) est testée pour déterminer si la connexion doit être autorisée.</span><span class="sxs-lookup"><span data-stu-id="c32bd-114">If this named value does not exist, the [**DefaultAccessPermission**](defaultaccesspermission.md) ACL is tested to determine whether the connection is to be allowed.</span></span>

<span data-ttu-id="c32bd-115">Pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou n’utilisent pas l’interface [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) pour spécifier l’AppID, l’exécutable du binaire de l’application doit être mappé à l’AppID de l’application, comme décrit dans [**AppID**](appid.md).</span><span class="sxs-lookup"><span data-stu-id="c32bd-115">For applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or do not use the [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) interface to specify the AppID, the executable of the application's binary must be mapped to the AppID of the application as described in [**AppID**](appid.md).</span></span> <span data-ttu-id="c32bd-116">Cela est nécessaire pour que COM puisse localiser l’AppID de l’application.</span><span class="sxs-lookup"><span data-stu-id="c32bd-116">This is required so that COM can locate the AppID of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c32bd-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c32bd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c32bd-118">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="c32bd-118">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="c32bd-119">**DefaultAccessPermission**</span><span class="sxs-lookup"><span data-stu-id="c32bd-119">**DefaultAccessPermission**</span></span>](defaultaccesspermission.md)
</dt> <dt>

[<span data-ttu-id="c32bd-120">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="c32bd-120">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 