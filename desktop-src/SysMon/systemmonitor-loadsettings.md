---
title: Méthode SystemMonitor. LoadSettings
description: Ajoute les compteurs dans le fichier de modèle HTML au moniteur système.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Méthode LoadSettings SysMon
- Méthode LoadSettings SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode LoadSettings
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384708"
---
# <a name="systemmonitorloadsettings-method"></a><span data-ttu-id="7dff6-106">Méthode SystemMonitor. LoadSettings</span><span class="sxs-lookup"><span data-stu-id="7dff6-106">SystemMonitor.LoadSettings method</span></span>

<span data-ttu-id="7dff6-107">Ajoute les compteurs dans le fichier de modèle HTML au moniteur système.</span><span class="sxs-lookup"><span data-stu-id="7dff6-107">Adds the counters in the HTML template file to the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dff6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dff6-108">Syntax</span></span>


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a><span data-ttu-id="7dff6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dff6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dff6-110">*SettingsFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dff6-110">*SettingsFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dff6-111">Chaîne HTML qui spécifie les compteurs à ajouter au moniteur système.</span><span class="sxs-lookup"><span data-stu-id="7dff6-111">HTML string that specifies the counters to add to the System Monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dff6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7dff6-112">Return value</span></span>

<span data-ttu-id="7dff6-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7dff6-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dff6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7dff6-114">Remarks</span></span>

<span data-ttu-id="7dff6-115">Pour enregistrer les compteurs actuels dans le moniteur système dans un fichier HTML, appelez la méthode [**systemmonitor. SaveAs**](systemmonitor-saveas.md) .</span><span class="sxs-lookup"><span data-stu-id="7dff6-115">To save the current counters in the System Monitor to an HTML file, call the [**SystemMonitor.SaveAs**](systemmonitor-saveas.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dff6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dff6-116">Requirements</span></span>



| <span data-ttu-id="7dff6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dff6-117">Requirement</span></span> | <span data-ttu-id="7dff6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dff6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dff6-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dff6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7dff6-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dff6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dff6-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dff6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7dff6-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dff6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dff6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7dff6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dff6-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="7dff6-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dff6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dff6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dff6-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="7dff6-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





