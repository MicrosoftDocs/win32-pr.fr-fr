---
title: RasAdminReleaseIpAddress fonction de rappel
description: La fonction RasAdminReleaseIpAddress est une fonction définie par l’application qui est exportée par une DLL d’administration de serveur RAS tierce.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Fonction de rappel RasAdminReleaseIpAddress RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729813"
---
# <a name="rasadminreleaseipaddress-callback-function"></a><span data-ttu-id="0f278-104">RasAdminReleaseIpAddress fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="0f278-104">RasAdminReleaseIpAddress callback function</span></span>

<span data-ttu-id="0f278-105">\[La fonction **RasAdminReleaseIpAddress** est disponible pour une utilisation dans Windows NT 4,0 et n’est pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f278-105">\[The **RasAdminReleaseIpAddress** function is available for use in Windows NT 4.0 and is unavailable in subsequent versions.</span></span> <span data-ttu-id="0f278-106">Utilisez plutôt [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span><span class="sxs-lookup"><span data-stu-id="0f278-106">Instead, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span></span>

<span data-ttu-id="0f278-107">La fonction **RasAdminReleaseIpAddress** est une fonction définie par l’application qui est exportée par une DLL d’administration de serveur RAS tierce.</span><span class="sxs-lookup"><span data-stu-id="0f278-107">The **RasAdminReleaseIpAddress** function is an application-defined function that is exported by a third-party RAS server administration DLL.</span></span> <span data-ttu-id="0f278-108">RAS appelle cette fonction pour notifier à la DLL que le client distant a été déconnecté et que l’adresse IP doit être libérée.</span><span class="sxs-lookup"><span data-stu-id="0f278-108">RAS calls this function to notify the DLL that the remote client was disconnected and that the IP address should be released.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f278-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f278-109">Syntax</span></span>


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a><span data-ttu-id="0f278-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f278-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f278-111">*lpszUserName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f278-111">*lpszUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f278-112">Spécifie le pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom d’un utilisateur distant pour lequel une adresse IP a été obtenue précédemment à l’aide de la fonction [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .</span><span class="sxs-lookup"><span data-stu-id="0f278-112">Specifies the pointer to a null-terminated Unicode string that specifies the name of a remote user for whom an IP address was previously obtained using the [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0f278-113">*lpszPortName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f278-113">*lpszPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f278-114">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du port sur lequel l’utilisateur spécifié par *lpszUserName* est connecté.</span><span class="sxs-lookup"><span data-stu-id="0f278-114">Pointer to a null-terminated Unicode string that specifies the name of the port on which the user specified by *lpszUserName* is connected.</span></span>

</dd> <dt>

<span data-ttu-id="0f278-115">*pipAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f278-115">*pipAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f278-116">Pointeur vers une variable **ipaddr** qui spécifie l’adresse IP renvoyée pour cet utilisateur lors d’un appel précédent à [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="0f278-116">Pointer to an **IPADDR** variable that specifies the IP address returned for this user in a previous call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f278-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f278-117">Return value</span></span>

<span data-ttu-id="0f278-118">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0f278-118">There is no extended error information for this function; do no call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f278-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0f278-119">Remarks</span></span>

<span data-ttu-id="0f278-120">Le serveur RAS appelle la fonction **RasAdminReleaseIpAddress** uniquement si l’application a retourné la **valeur true** dans le paramètre *bNotifyRelease* au cours de l’appel précédent à [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) pour l’utilisateur spécifié par le paramètre *lpszUserName* .</span><span class="sxs-lookup"><span data-stu-id="0f278-120">The RAS server calls the **RasAdminReleaseIpAddress** function only if the application returned **TRUE** in the *bNotifyRelease* parameter during the earlier call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) for the user specified by the *lpszUserName* parameter.</span></span>

<span data-ttu-id="0f278-121">Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant les informations sous la clé suivante dans le registre :</span><span class="sxs-lookup"><span data-stu-id="0f278-121">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="0f278-122">Pour inscrire la DLL, définissez les valeurs suivantes sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="0f278-122">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="0f278-123">Nom de la valeur</span><span class="sxs-lookup"><span data-stu-id="0f278-123">Value name</span></span>    | <span data-ttu-id="0f278-124">Données de valeur</span><span class="sxs-lookup"><span data-stu-id="0f278-124">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="0f278-125">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="0f278-125">*DisplayName*</span></span> | <span data-ttu-id="0f278-126">Chaîne **\_ SZ reg** qui contient le nom complet convivial de la dll.</span><span class="sxs-lookup"><span data-stu-id="0f278-126">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="0f278-127">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="0f278-127">*DLLPath*</span></span>     | <span data-ttu-id="0f278-128">Chaîne **\_ SZ reg** contenant le chemin d’accès complet de la dll.</span><span class="sxs-lookup"><span data-stu-id="0f278-128">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="0f278-129">Par exemple, l’entrée de Registre pour une DLL d’administration RAS d’une société fictive nommée ProElectron, Inc. peut être :</span><span class="sxs-lookup"><span data-stu-id="0f278-129">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="0f278-130">*DisplayName*: **reg \_ SZ** : dll d’administration du service d’accès distant diselectron *DllPath*: **reg \_ SZ** : C : \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="0f278-130">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL *DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="0f278-131">Le programme d’installation d’une DLL d’administration RAS doit également fournir des fonctionnalités de suppression/désinstallation.</span><span class="sxs-lookup"><span data-stu-id="0f278-131">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="0f278-132">Si un utilisateur supprime la DLL, le programme d’installation doit supprimer les entrées de registre de la DLL.</span><span class="sxs-lookup"><span data-stu-id="0f278-132">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 