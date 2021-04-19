---
description: Retourne un objet RecordList qui répertorie les composants installés.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Installer. ComponentsEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539976"
---
# <a name="installercomponentsex-property"></a><span data-ttu-id="cf1b6-103">Installer. ComponentsEx, propriété</span><span class="sxs-lookup"><span data-stu-id="cf1b6-103">Installer.ComponentsEx property</span></span>

<span data-ttu-id="cf1b6-104">Cette propriété retourne un objet [**RecordList**](recordlist-object.md) qui répertorie les composants installés.</span><span class="sxs-lookup"><span data-stu-id="cf1b6-104">This property returns a [**RecordList**](recordlist-object.md) object that lists installed components.</span></span> <span data-ttu-id="cf1b6-105">Cette propriété appelle [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span><span class="sxs-lookup"><span data-stu-id="cf1b6-105">This property calls [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span></span>

<span data-ttu-id="cf1b6-106">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cf1b6-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="cf1b6-107">Cette propriété est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="cf1b6-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="cf1b6-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cf1b6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf1b6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf1b6-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a><span data-ttu-id="cf1b6-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cf1b6-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="cf1b6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf1b6-111">Requirements</span></span>



| <span data-ttu-id="cf1b6-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf1b6-112">Requirement</span></span> | <span data-ttu-id="cf1b6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf1b6-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1b6-114">Version</span><span class="sxs-lookup"><span data-stu-id="cf1b6-114">Version</span></span><br/> | <span data-ttu-id="cf1b6-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf1b6-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="cf1b6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="cf1b6-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf1b6-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b6-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="cf1b6-118">IID</span><span class="sxs-lookup"><span data-stu-id="cf1b6-118">IID</span></span><br/>     | <span data-ttu-id="cf1b6-119">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cf1b6-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="cf1b6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf1b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1b6-121">**MsiEnumComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="cf1b6-121">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




