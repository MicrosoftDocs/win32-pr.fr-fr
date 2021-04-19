---
title: Méthode IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread
description: Cette API déterminera si le jeton du contexte actuel a accès à la classe d’interface de périphérique spécifiée. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Méthode DeviceInterfaceClassAccessCheckWithCallingThread API Broker d’accès du périphérique
- Méthode DeviceInterfaceClassAccessCheckWithCallingThread API Broker d’accès du périphérique, interface IDeviceAccessPolicyCheck
- API Broker d’accès du périphérique de l’interface IDeviceAccessPolicyCheck, méthode DeviceInterfaceClassAccessCheckWithCallingThread
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "106527553"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a><span data-ttu-id="50e6f-107">IDeviceAccessPolicyCheck ::D méthode eviceInterfaceClassAccessCheckWithCallingThread</span><span class="sxs-lookup"><span data-stu-id="50e6f-107">IDeviceAccessPolicyCheck::DeviceInterfaceClassAccessCheckWithCallingThread method</span></span>

> [!Important]  
> <span data-ttu-id="50e6f-108">Ces interfaces ne sont pas prises en charge et ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="50e6f-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="50e6f-109">Utilisez plutôt les API dans la [référence de programmation C++ de l’API d’accès à l’appareil](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="50e6f-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="50e6f-110">Cette API déterminera si le jeton du contexte actuel a accès à la classe d’interface de périphérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="50e6f-110">This API will determine if the token for the current context has access to the device interface class specified.</span></span> <span data-ttu-id="50e6f-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span><span class="sxs-lookup"><span data-stu-id="50e6f-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e6f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50e6f-112">Syntax</span></span>

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a><span data-ttu-id="50e6f-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50e6f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e6f-114">*pszDeviceInterfaceClassGuid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50e6f-114">*pszDeviceInterfaceClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e6f-115">GUID de la classe d’interface de l’appareil pour lequel l’accès doit être vérifié.</span><span class="sxs-lookup"><span data-stu-id="50e6f-115">Device interface class GUID for which access should be checked.</span></span>

</dd> <dt>

<span data-ttu-id="50e6f-116">*dwClientThreadId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50e6f-116">*dwClientThreadId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e6f-117">ID de thread client où toute interface utilisateur associée doit être affichée si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="50e6f-117">Client thread ID where any associated UI should be shown if necessary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e6f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50e6f-118">Return value</span></span>

<span data-ttu-id="50e6f-119">Si cette fonction est réussie, elle retourne S_OK.</span><span class="sxs-lookup"><span data-stu-id="50e6f-119">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="50e6f-120">Sinon, elle retourne un code d’erreur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="50e6f-120">Otherwise, it returns an HRESULT error code.</span></span>
