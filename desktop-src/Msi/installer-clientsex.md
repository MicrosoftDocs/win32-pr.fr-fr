---
description: Retourne un objet RecordList qui répertorie les produits qui utilisent un composant installé spécifié.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Installer. ClientsEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544101"
---
# <a name="installerclientsex-property"></a><span data-ttu-id="5e039-103">Installer. ClientsEx, propriété</span><span class="sxs-lookup"><span data-stu-id="5e039-103">Installer.ClientsEx property</span></span>

<span data-ttu-id="5e039-104">Cette propriété retourne un objet [**RecordList**](recordlist-object.md) qui répertorie les produits qui utilisent un composant installé spécifié.</span><span class="sxs-lookup"><span data-stu-id="5e039-104">This property returns a [**RecordList**](recordlist-object.md) object that lists products that use a specified installed component.</span></span> <span data-ttu-id="5e039-105">Cette propriété appelle [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span><span class="sxs-lookup"><span data-stu-id="5e039-105">This property calls [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span></span>

<span data-ttu-id="5e039-106">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e039-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="5e039-107">Cette propriété est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e039-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="5e039-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5e039-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e039-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e039-109">Syntax</span></span>


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a><span data-ttu-id="5e039-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5e039-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5e039-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e039-111">Requirements</span></span>



| <span data-ttu-id="5e039-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e039-112">Requirement</span></span> | <span data-ttu-id="5e039-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e039-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e039-114">Version</span><span class="sxs-lookup"><span data-stu-id="5e039-114">Version</span></span><br/> | <span data-ttu-id="5e039-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="5e039-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="5e039-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5e039-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="5e039-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e039-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="5e039-118">IID</span><span class="sxs-lookup"><span data-stu-id="5e039-118">IID</span></span><br/>     | <span data-ttu-id="5e039-119">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5e039-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="5e039-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e039-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e039-121">**MsiEnumClientsEx**</span><span class="sxs-lookup"><span data-stu-id="5e039-121">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




