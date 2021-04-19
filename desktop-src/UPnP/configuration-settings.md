---
title: Paramètres de configuration
description: Le comportement de l’API du point de contrôle et de l’API de l’hôte du périphérique peut être modifié en modifiant les paramètres du Registre.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510810"
---
# <a name="configuration-settings"></a><span data-ttu-id="a7b25-103">Paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="a7b25-103">Configuration Settings</span></span>

<span data-ttu-id="a7b25-104">Le comportement de l' [API du point de contrôle](control-point-api.md) et de l’API de l' [hôte du périphérique](device-host-api.md) peut être modifié en modifiant les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="a7b25-104">The behavior of the [Control Point API](control-point-api.md) and [Device Host API](device-host-api.md) can be modified by changing settings in the registry.</span></span>

<span data-ttu-id="a7b25-105">Sept valeurs de Registre affectent le comportement :</span><span class="sxs-lookup"><span data-stu-id="a7b25-105">There are seven registry values that affect behavior:</span></span>

-   <span data-ttu-id="a7b25-106">**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="a7b25-106">**DownloadScope**</span></span>
-   <span data-ttu-id="a7b25-107">**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="a7b25-107">**DeviceLifeTime**</span></span>
-   <span data-ttu-id="a7b25-108">\\Hôte d’appareil **UPnP** \\ **Limite de taille de fichier**</span><span class="sxs-lookup"><span data-stu-id="a7b25-108">\\**UPnP Device Host**\\**File Size Limit**</span></span>
-   <span data-ttu-id="a7b25-109">\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de taille de fichier**</span><span class="sxs-lookup"><span data-stu-id="a7b25-109">\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
-   <span data-ttu-id="a7b25-110">**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="a7b25-110">**MaxCache**</span></span>
-   <span data-ttu-id="a7b25-111">**TTL**</span><span class="sxs-lookup"><span data-stu-id="a7b25-111">**TTL**</span></span>
-   <span data-ttu-id="a7b25-112">**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="a7b25-112">**ReceiveScope**</span></span>

<span data-ttu-id="a7b25-113">Il existe deux valeurs de Registre appelées **limite de taille de fichier**, une pour les documents de description et l’autre pour les réponses qui utilisent le protocole SOAP (Simple Object Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="a7b25-113">There are two registry values called **File Size Limit**, one for description documents and the other for responses that use Simple Object Access Protocol (SOAP).</span></span>

<span data-ttu-id="a7b25-114">L’emplacement de chacune des sept valeurs dans le Registre est le suivant :</span><span class="sxs-lookup"><span data-stu-id="a7b25-114">The location of each of the seven values in the registry is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a><span data-ttu-id="a7b25-115">Descriptions des valeurs de Registre</span><span class="sxs-lookup"><span data-stu-id="a7b25-115">Registry Value Descriptions</span></span>

<span data-ttu-id="a7b25-116">Les valeurs de Registre sont expliquées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="a7b25-116">The registry values are explained in the following list.</span></span> <span data-ttu-id="a7b25-117">Chaque valeur de Registre est un nombre **\_ DWORD reg** (un entier 32 bits).</span><span class="sxs-lookup"><span data-stu-id="a7b25-117">Each registry value is a **REG\_DWORD** (a 32-bit integer).</span></span> <span data-ttu-id="a7b25-118">L’effet de chaque valeur est global.</span><span class="sxs-lookup"><span data-stu-id="a7b25-118">The effect of each value is global.</span></span>

<dl> <dt>

<span data-ttu-id="a7b25-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="a7b25-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span></span>
</dt> <dd>

<span data-ttu-id="a7b25-120">Spécifie les adresses IP valides pour l’URL du document de description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b25-120">Specifies which IP addresses are valid for the device description document URL.</span></span> <span data-ttu-id="a7b25-121">Si l’adresse IP de l’hôte spécifié dans l’URL du document de description ne se trouve pas dans l’étendue spécifiée par **DownloadScope**, cette adresse IP n’est pas valide et l’objet de l’appareil n’est pas créé.</span><span class="sxs-lookup"><span data-stu-id="a7b25-121">If the IP address of the host that is specified in the description document URL is not within the scope specified by **DownloadScope**, that IP address is not valid and the device object will not be created.</span></span>

<span data-ttu-id="a7b25-122">Les valeurs valides sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7b25-122">The valid values are shown in the following table.</span></span> <span data-ttu-id="a7b25-123">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="a7b25-123">The default value is 1.</span></span>



| <span data-ttu-id="a7b25-124">Valeur de **DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="a7b25-124">Value of **DownloadScope**</span></span> | <span data-ttu-id="a7b25-125">Signification</span><span class="sxs-lookup"><span data-stu-id="a7b25-125">Meaning</span></span>                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b25-126">0</span><span class="sxs-lookup"><span data-stu-id="a7b25-126">0</span></span>                          | <span data-ttu-id="a7b25-127">L’adresse IP de l’hôte doit être une adresse de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="a7b25-127">Host's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="a7b25-128">1</span><span class="sxs-lookup"><span data-stu-id="a7b25-128">1</span></span>                          | <span data-ttu-id="a7b25-129">L’adresse IP de l’hôte doit être une adresse de sous-réseau ou une adresse privée de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (comme spécifié par la norme RFC 1918) ou 169,254. *x*. *x* (comme spécifié par la norme RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="a7b25-129">Host's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="a7b25-130">2</span><span class="sxs-lookup"><span data-stu-id="a7b25-130">2</span></span>                          | <span data-ttu-id="a7b25-131">L’adresse IP de l’hôte doit être une adresse de sous-réseau, une adresse privée ou une adresse qui se trouve dans les tronçons de durée de vie (TTL) du point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a7b25-131">Host's IP address must be a subnet address, private address, or an address that is within the time-to-live (TTL) hops from the control point.</span></span>                                                              |
| <span data-ttu-id="a7b25-132">3</span><span class="sxs-lookup"><span data-stu-id="a7b25-132">3</span></span>                          | <span data-ttu-id="a7b25-133">L’adresse IP de l’hôte peut être n’importe quelle adresse.</span><span class="sxs-lookup"><span data-stu-id="a7b25-133">Host's IP address can be any address.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="a7b25-134">>3</span><span class="sxs-lookup"><span data-stu-id="a7b25-134">>3</span></span>                      | <span data-ttu-id="a7b25-135">Identique à celui de la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="a7b25-135">Same as that for the value 0.</span></span>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="a7b25-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="a7b25-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span></span>
</dt> <dd>

<span data-ttu-id="a7b25-137">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a7b25-137">Optional.</span></span> <span data-ttu-id="a7b25-138">Spécifie la durée de vie d’un appareil, en secondes, qui remplace la valeur fournie dans le message d’annonce de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b25-138">Specifies a device's lifetime, in seconds, which overrides the value provided in the device's announcement message.</span></span> <span data-ttu-id="a7b25-139">Si **DeviceLifeTime** est présent, la valeur spécifiée dans l’annonce de l’appareil est ignorée et la valeur de Registre est utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="a7b25-139">If **DeviceLifeTime** is present, the value specified in the device's announcement is ignored and the registry value is used instead.</span></span> <span data-ttu-id="a7b25-140">Cela s’applique à tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="a7b25-140">This applies to all devices.</span></span>

<span data-ttu-id="a7b25-141">Les valeurs valides sont comprises entre 900 et **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="a7b25-141">Valid values range from 900 through **MAX\_DWORD**.</span></span> <span data-ttu-id="a7b25-142">La valeur par défaut est 1800.</span><span class="sxs-lookup"><span data-stu-id="a7b25-142">The default value is 1800.</span></span> <span data-ttu-id="a7b25-143">Si **DeviceLifeTime** est défini sur 0, la valeur par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a7b25-143">If **DeviceLifeTime** is set to 0, the default value is used.</span></span>

</dd> <dt>

<span data-ttu-id="a7b25-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\Hôte d’appareil **UPnP** \\ **Limite de taille de fichier**</span><span class="sxs-lookup"><span data-stu-id="a7b25-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP Device Host**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="a7b25-145">Spécifie la taille maximale, en octets, de chaque document de description.</span><span class="sxs-lookup"><span data-stu-id="a7b25-145">Specifies the maximum size, in bytes, of each description document.</span></span> <span data-ttu-id="a7b25-146">Ce paramètre n’est pas configurable dans les versions de Windows antérieures à Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="a7b25-146">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="a7b25-147">Dans les versions précédentes, ce paramètre est codé en dur en tant que 102400.</span><span class="sxs-lookup"><span data-stu-id="a7b25-147">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="a7b25-148">Les valeurs valides sont comprises entre 10240 et **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="a7b25-148">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="a7b25-149">La valeur par défaut est 102400.</span><span class="sxs-lookup"><span data-stu-id="a7b25-149">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="a7b25-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de taille de fichier**</span><span class="sxs-lookup"><span data-stu-id="a7b25-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="a7b25-151">Spécifie la taille maximale, en octets, de la réponse SOAP acceptable.</span><span class="sxs-lookup"><span data-stu-id="a7b25-151">Specifies the maximum size, in bytes, of the SOAP response that is acceptable.</span></span> <span data-ttu-id="a7b25-152">Ce paramètre n’est pas configurable dans les versions de Windows antérieures à Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="a7b25-152">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="a7b25-153">Dans les versions précédentes, ce paramètre est codé en dur en tant que 102400.</span><span class="sxs-lookup"><span data-stu-id="a7b25-153">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="a7b25-154">Les valeurs valides sont comprises entre 10240 et **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="a7b25-154">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="a7b25-155">La valeur par défaut est 102400.</span><span class="sxs-lookup"><span data-stu-id="a7b25-155">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="a7b25-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="a7b25-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span></span>
</dt> <dd>

<span data-ttu-id="a7b25-157">Spécifie le nombre maximal d’entrées autorisées dans le cache SSDP (simple service Discovery Protocol).</span><span class="sxs-lookup"><span data-stu-id="a7b25-157">Specifies the maximum number of entries allowed in the Simple Service Discovery Protocol (SSDP) cache.</span></span>

<span data-ttu-id="a7b25-158">Les valeurs valides sont comprises entre 10 et 30000.</span><span class="sxs-lookup"><span data-stu-id="a7b25-158">Valid values range from 10 through 30000.</span></span> <span data-ttu-id="a7b25-159">La valeur par défaut est 1000.</span><span class="sxs-lookup"><span data-stu-id="a7b25-159">The default value is 1000.</span></span>

</dd> <dt>

<span data-ttu-id="a7b25-160"><span id="TTL"></span><span id="ttl"></span>**EXPIRATION**</span><span class="sxs-lookup"><span data-stu-id="a7b25-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span></span>
</dt> <dd>

<span data-ttu-id="a7b25-161">Spécifie la durée de vie d’un paquet SSDP.</span><span class="sxs-lookup"><span data-stu-id="a7b25-161">Specifies the time-to-live for an SSDP packet.</span></span> <span data-ttu-id="a7b25-162">Autrement dit, la **durée de vie** spécifie le nombre de tronçons autorisés pour un paquet.</span><span class="sxs-lookup"><span data-stu-id="a7b25-162">That is, **TTL** specifies the number of hops allowed for a packet.</span></span>

<span data-ttu-id="a7b25-163">Les valeurs valides sont comprises entre 1 et 255.</span><span class="sxs-lookup"><span data-stu-id="a7b25-163">Valid values range from 1 through 255.</span></span> <span data-ttu-id="a7b25-164">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="a7b25-164">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="a7b25-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="a7b25-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span></span>
</dt> <dd>

<span data-ttu-id="a7b25-166">Spécifie les adresses IP qui sont des sources valides d’un message.</span><span class="sxs-lookup"><span data-stu-id="a7b25-166">Specifies which IP addresses are valid sources of a message.</span></span> <span data-ttu-id="a7b25-167">Si un message entrant provient d’une adresse qui ne se trouve pas dans l’étendue spécifiée par **ReceiveScope**, le message est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a7b25-167">If an incoming message originates from an address that is not within the scope specified by **ReceiveScope**, the message is ignored.</span></span> <span data-ttu-id="a7b25-168">Ce paramètre n’est pas configurable dans les versions de Windows antérieures à Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="a7b25-168">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="a7b25-169">Dans les versions précédentes, un message est accepté sans tenir compte de sa source.</span><span class="sxs-lookup"><span data-stu-id="a7b25-169">In the previous versions, a message is accepted without regard to its source.</span></span>

<span data-ttu-id="a7b25-170">Les valeurs valides sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7b25-170">The valid values are shown in the following table.</span></span> <span data-ttu-id="a7b25-171">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="a7b25-171">The default value is 1.</span></span>



| <span data-ttu-id="a7b25-172">Valeur de **ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="a7b25-172">Value of **ReceiveScope**</span></span> | <span data-ttu-id="a7b25-173">Signification</span><span class="sxs-lookup"><span data-stu-id="a7b25-173">Meaning</span></span>                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b25-174">0</span><span class="sxs-lookup"><span data-stu-id="a7b25-174">0</span></span>                         | <span data-ttu-id="a7b25-175">L’adresse IP de l’expéditeur doit être une adresse de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="a7b25-175">Sender's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="a7b25-176">1</span><span class="sxs-lookup"><span data-stu-id="a7b25-176">1</span></span>                         | <span data-ttu-id="a7b25-177">L’adresse IP de l’expéditeur doit être une adresse de sous-réseau ou une adresse privée de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (comme spécifié par la norme RFC 1918) ou 169,254. *x*. *x* (comme spécifié par la norme RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="a7b25-177">Sender's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="a7b25-178">2</span><span class="sxs-lookup"><span data-stu-id="a7b25-178">2</span></span>                         | <span data-ttu-id="a7b25-179">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a7b25-179">Not used.</span></span> <span data-ttu-id="a7b25-180">Si **ReceiveScope** a la valeur 2, la valeur par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a7b25-180">If **ReceiveScope** is set to 2, the default value is used.</span></span>                                                                                                                                        |
| <span data-ttu-id="a7b25-181">3</span><span class="sxs-lookup"><span data-stu-id="a7b25-181">3</span></span>                         | <span data-ttu-id="a7b25-182">L’adresse IP de l’expéditeur peut être n’importe quelle adresse.</span><span class="sxs-lookup"><span data-stu-id="a7b25-182">Sender's IP address can be any address.</span></span>                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a7b25-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7b25-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7b25-184">Vue d’ensemble de l’architecture UPnP</span><span class="sxs-lookup"><span data-stu-id="a7b25-184">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




