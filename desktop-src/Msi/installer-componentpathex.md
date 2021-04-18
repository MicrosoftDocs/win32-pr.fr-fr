---
description: Retourne un objet RecordList qui donne le chemin d’accès complet d’un composant installé spécifié.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Installer. ComponentPathEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526533"
---
# <a name="installercomponentpathex-property"></a><span data-ttu-id="c0d4f-103">Installer. ComponentPathEx, propriété</span><span class="sxs-lookup"><span data-stu-id="c0d4f-103">Installer.ComponentPathEx property</span></span>

<span data-ttu-id="c0d4f-104">Cette propriété retourne un objet [**RecordList**](recordlist-object.md) qui donne le chemin d’accès complet d’un composant installé spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0d4f-104">This property returns a [**RecordList**](recordlist-object.md) object that gives the full path of a specified installed component.</span></span> <span data-ttu-id="c0d4f-105">Cette propriété appelle [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span><span class="sxs-lookup"><span data-stu-id="c0d4f-105">This property calls [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span></span>

<span data-ttu-id="c0d4f-106">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c0d4f-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="c0d4f-107">Cette propriété est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="c0d4f-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="c0d4f-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0d4f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d4f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0d4f-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a><span data-ttu-id="c0d4f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c0d4f-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c0d4f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0d4f-111">Requirements</span></span>



| <span data-ttu-id="c0d4f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0d4f-112">Requirement</span></span> | <span data-ttu-id="c0d4f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0d4f-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d4f-114">Version</span><span class="sxs-lookup"><span data-stu-id="c0d4f-114">Version</span></span><br/> | <span data-ttu-id="c0d4f-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0d4f-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="c0d4f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c0d4f-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0d4f-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0d4f-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="c0d4f-118">IID</span><span class="sxs-lookup"><span data-stu-id="c0d4f-118">IID</span></span><br/>     | <span data-ttu-id="c0d4f-119">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c0d4f-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c0d4f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0d4f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d4f-121">**MsiGetComponentPathEx**</span><span class="sxs-lookup"><span data-stu-id="c0d4f-121">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




