---
description: Indique si une adresse réseau est conforme à un type et un format spécifiés.
title: Message NCM_GETADDRESS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972311"
---
# <a name="ncm_getaddress-message"></a><span data-ttu-id="05122-103">\_Message NCM GETADDRESS</span><span class="sxs-lookup"><span data-stu-id="05122-103">NCM\_GETADDRESS message</span></span>

<span data-ttu-id="05122-104">Indique si une adresse réseau est conforme à un type et un format spécifiés.</span><span class="sxs-lookup"><span data-stu-id="05122-104">Indicates whether a network address conforms to a specified type and format.</span></span>


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="05122-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05122-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05122-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05122-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="05122-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="05122-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="05122-108">*PV* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="05122-108">*pv* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="05122-109">Pointeur vers une structure <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> pour recevoir des informations d’adresse réseau sous forme analysée, si le format et le type d’adresse dans le contrôle spécifié par *HWND* sont validés.</span><span class="sxs-lookup"><span data-stu-id="05122-109">A pointer to an <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by *hwnd* are validated.</span></span> <span data-ttu-id="05122-110">L’application appelante est chargée d’allouer la mémoire pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="05122-110">The calling application is responsible for allocating the memory for this structure.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05122-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05122-111">Return value</span></span>

<span data-ttu-id="05122-112">Retourne l’une des valeurs suivantes de type **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="05122-112">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="05122-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="05122-113">Return code</span></span>                                                                                                | <span data-ttu-id="05122-114">Description</span><span class="sxs-lookup"><span data-stu-id="05122-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05122-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05122-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="05122-116">L’application appelante n’a pas pu allouer une structure d' [**\_ adresse NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .</span><span class="sxs-lookup"><span data-stu-id="05122-116">The calling application failed to allocate a [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure.</span></span><br/> |
| <dl> <span data-ttu-id="05122-117"><dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="05122-117"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="05122-118">La mémoire tampon de sortie est trop petite pour contenir l’adresse réseau analysée.</span><span class="sxs-lookup"><span data-stu-id="05122-118">The out buffer is too small to hold the parsed network address.</span></span><br/>                           |
| <dl> <span data-ttu-id="05122-119"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05122-119"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="05122-120">La chaîne d’adresse réseau n’est pas de type spécifié.</span><span class="sxs-lookup"><span data-stu-id="05122-120">The network address string is not of any type specified.</span></span><br/>                                  |
| <dl> <span data-ttu-id="05122-121"><dt>**ERREUR de \_ réussite**</dt></span><span class="sxs-lookup"><span data-stu-id="05122-121"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="05122-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="05122-122">The operation was successful.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="05122-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="05122-123"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="05122-124">Il n’y a aucune adresse dans le contrôle d’adresse réseau à valider.</span><span class="sxs-lookup"><span data-stu-id="05122-124">There is no address in the network address control to validate.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="05122-125">Notes</span><span class="sxs-lookup"><span data-stu-id="05122-125">Remarks</span></span>

<span data-ttu-id="05122-126">Utilisez le message **NCM \_ GETADDRESS** pour valider une adresse réseau dans un contrôle d’adresse réseau par rapport à un masque de type d’adresse réseau prédéfini.</span><span class="sxs-lookup"><span data-stu-id="05122-126">Use the **NCM\_GETADDRESS** message to validate a network address in a network address control against a preset network address type mask.</span></span> <span data-ttu-id="05122-127">Pour instancier, utilisez la classe **msctls \_ NetAddress** définie dans shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="05122-127">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="05122-128">Appelez [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) au moment de l’exécution avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="05122-128">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="05122-129">Cette commande initialise la bibliothèque de contrôles communs qui contient le contrôle d’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="05122-129">This initializes the common controls library that contains the network address control.</span></span>

<span data-ttu-id="05122-130">Ce message obtient la chaîne d’adresse réseau à partir d’un contrôle d’adresse réseau, analyse la chaîne et vérifie si la chaîne correspond à un masque de type d’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="05122-130">This message gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask.</span></span> <span data-ttu-id="05122-131">Si la chaîne correspond au masque, le message retourne \_ la valeur OK et retourne la chaîne sous forme analysée à l’application appelante (y compris le numéro de port, la longueur de préfixe et d’autres informations d’adresse), à l’aide de la structure d' [**\_ adresse NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) pointée par *va*.</span><span class="sxs-lookup"><span data-stu-id="05122-131">If the string matches the mask, the message returns S\_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure pointed to by *pv*.</span></span> <span data-ttu-id="05122-132">Ce message renvoie E \_ INVALIDARG si l’application appelante ne parvient pas à allouer la structure désignée par *va*.</span><span class="sxs-lookup"><span data-stu-id="05122-132">This message returns E\_INVALIDARG if the calling application fails to allocate the structure pointed to by *pv*.</span></span>

<span data-ttu-id="05122-133">Les représentations de l’adresse IP (Internet Protocol) versions 4 et 6 (v4/V6) pour les services et les réseaux, ainsi que les adresses Internet et les services nommés utilisant le format DNS (Domain Name System) sont analysés.</span><span class="sxs-lookup"><span data-stu-id="05122-133">Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed.</span></span> <span data-ttu-id="05122-134">Si la chaîne d’adresse réseau représente un nom d’hôte (DNS) ou un service nommé, la valeur retournée dans le membre **PrefixLength** de l' [**\_ adresse NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="05122-134">If the network address string represents a named host name (DNS) or service, the value returned in the **PrefixLength** member of [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) is zero.</span></span>

<span data-ttu-id="05122-135">Définissez le masque de type d’adresse réseau à l’aide du message [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) avant d’envoyer la macro **NCM \_ GETADDRESS** .</span><span class="sxs-lookup"><span data-stu-id="05122-135">Set the network address type mask using the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message before you send the **NCM\_GETADDRESS** macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="05122-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="05122-136">Requirements</span></span>



| <span data-ttu-id="05122-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05122-137">Requirement</span></span> | <span data-ttu-id="05122-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="05122-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05122-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05122-139">Minimum supported client</span></span><br/> | <span data-ttu-id="05122-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05122-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05122-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05122-141">Minimum supported server</span></span><br/> | <span data-ttu-id="05122-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05122-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05122-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="05122-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="05122-144"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="05122-144"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05122-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05122-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05122-146">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="05122-146">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="05122-147">**GetAddress NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="05122-147">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




