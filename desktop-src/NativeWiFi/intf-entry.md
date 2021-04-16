---
description: Contient des informations détaillées sur une interface requise par un client RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: Structure INTF_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527651"
---
# <a name="intf_entry-structure"></a><span data-ttu-id="8419e-103">\_Structure d’entrée INTF</span><span class="sxs-lookup"><span data-stu-id="8419e-103">INTF\_ENTRY structure</span></span>

<span data-ttu-id="8419e-104">\[**INTF \_ L’entrée** n’est plus prise en charge à partir de Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8419e-104">\[**INTF\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8419e-105">Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires.</span><span class="sxs-lookup"><span data-stu-id="8419e-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="8419e-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="8419e-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="8419e-107">Contient des informations détaillées sur une interface requise par un client RPC.</span><span class="sxs-lookup"><span data-stu-id="8419e-107">Contains detailed information about an interface that is required by an RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="8419e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8419e-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a><span data-ttu-id="8419e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8419e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8419e-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="8419e-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-111">Pointeur vers le GUID d’interface représenté sous la forme d’une chaîne Unicode au format suivant : "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="8419e-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> <dt>

<span data-ttu-id="8419e-112">**wszDescr**</span><span class="sxs-lookup"><span data-stu-id="8419e-112">**wszDescr**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-113">Pointeur vers une chaîne qui contient la description d’interface récupérée par le service de configuration automatique sans fil (WZCSVC).</span><span class="sxs-lookup"><span data-stu-id="8419e-113">A pointer to a string that contains the interface description that is retrieved by the Wireless Zero Configuration service (WZCSVC).</span></span>

</dd> <dt>

<span data-ttu-id="8419e-114">**dwContext**</span><span class="sxs-lookup"><span data-stu-id="8419e-114">**dwContext**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-115">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="8419e-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-116">**ulMediaState**</span><span class="sxs-lookup"><span data-stu-id="8419e-116">**ulMediaState**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-117">État de connexion du média NDIS actuel pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-117">The current NDIS media connect state for the interface.</span></span> <span data-ttu-id="8419e-118">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="8419e-118">The following table shows the possible values.</span></span>



| <span data-ttu-id="8419e-119">Value</span><span class="sxs-lookup"><span data-stu-id="8419e-119">Value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="8419e-120">Signification</span><span class="sxs-lookup"><span data-stu-id="8419e-120">Meaning</span></span>                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <span data-ttu-id="8419e-121"><dt> **État du support \_ \_ connecté**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-121"><dt>**MEDIA\_STATE\_CONNECTED** </dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="8419e-122">Le média est connecté.</span><span class="sxs-lookup"><span data-stu-id="8419e-122">The media is connected.</span></span><br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <span data-ttu-id="8419e-123"><dt>**Éléments multimédias \_ ÉTAT \_ déconnecté**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-123"><dt>**MEDIA\_STATE\_DISCONNECTED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="8419e-124">Le média est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="8419e-124">The media is disconnected.</span></span><br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <span data-ttu-id="8419e-125"><dt>**Éléments multimédias \_ ÉTAT \_ inconnu**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-125"><dt>**MEDIA\_STATE\_UNKNOWN**</dt> <dt>-1</dt></span></span> </dl>               | <span data-ttu-id="8419e-126">L’état du support est inconnu.</span><span class="sxs-lookup"><span data-stu-id="8419e-126">The media state is unknown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8419e-127">**ulMediaType**</span><span class="sxs-lookup"><span data-stu-id="8419e-127">**ulMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-128">Types de média NDIS que la carte réseau utilise actuellement.</span><span class="sxs-lookup"><span data-stu-id="8419e-128">The NDIS media types that the NIC currently uses.</span></span> <span data-ttu-id="8419e-129">Lorsqu’il est interrogé, la valeur de ce membre est **NdisMedium802 \_ 3** , comme défini dans le fichier d’en-tête *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="8419e-129">When queried, the value of this member is **NdisMedium802\_3** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-130">**ulPhysicalMediaType**</span><span class="sxs-lookup"><span data-stu-id="8419e-130">**ulPhysicalMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-131">Type de média NDIS pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-131">The NDIS media type for the interface.</span></span> <span data-ttu-id="8419e-132">Lors de la requête, la valeur de ce membre est **NdisPhysicalMediumWirelessLan** comme défini dans le fichier d’en-tête *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="8419e-132">When queried, the value of this member is **NdisPhysicalMediumWirelessLan** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-133">**nInfraMode**</span><span class="sxs-lookup"><span data-stu-id="8419e-133">**nInfraMode**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-134">Mode d’infrastructure actuel 802,11 défini sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-134">The current 802.11 Infrastructure Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-135">**nAuthMode**</span><span class="sxs-lookup"><span data-stu-id="8419e-135">**nAuthMode**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-136">Mode d’authentification 802,11 actuel défini sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-136">The current 802.11 Authentication Mode set on the interface.</span></span>

<span data-ttu-id="8419e-137">Le tableau suivant indique les valeurs possibles pour le paramètre en fonction de l’énumération du **\_ \_ \_ \_ mode d’authentification NDIS 802 11** définie dans le fichier d’en-tête *NtDDNdis. h* .</span><span class="sxs-lookup"><span data-stu-id="8419e-137">The following table shows the possible values for the parameter based on the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration defined in the *NtDDNdis.h* header file.</span></span>



| <span data-ttu-id="8419e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="8419e-138">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="8419e-139">Signification</span><span class="sxs-lookup"><span data-stu-id="8419e-139">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <span data-ttu-id="8419e-140"><dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-140"><dt>**Ndis802\_11AuthModeOpen**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="8419e-141">Authentification système Open IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="8419e-141">IEEE 802.11 Open System authentication.</span></span><br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <span data-ttu-id="8419e-142"><dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-142"><dt>**Ndis802\_11AuthModeShared**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="8419e-143">Authentification partagée IEEE 802,11 qui utilise une clé WEP (Wired Equivalent Privacy) prépartagée.</span><span class="sxs-lookup"><span data-stu-id="8419e-143">IEEE 802.11 shared authentication that uses a pre-shared wired equivalent privacy (WEP) key.</span></span> <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <span data-ttu-id="8419e-144"><dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-144"><dt>**Ndis802\_11AuthModeAutoSwitch**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="8419e-145">Mode de basculement automatique.</span><span class="sxs-lookup"><span data-stu-id="8419e-145">Auto-switch mode.</span></span> <span data-ttu-id="8419e-146">Lorsque vous utilisez le mode de basculement automatique, la carte d’interface réseau (NIC) sans fil tente d’abord d’utiliser le mode d’authentification partagé.</span><span class="sxs-lookup"><span data-stu-id="8419e-146">When using auto-switch mode, the wireless network interface card (NIC) tries shared authentication mode first.</span></span> <span data-ttu-id="8419e-147">Si le mode partagé échoue, la carte réseau tente d’utiliser le mode d’authentification ouvert.</span><span class="sxs-lookup"><span data-stu-id="8419e-147">If shared mode fails, the NIC attempts to use open authentication mode.</span></span> <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <span data-ttu-id="8419e-148"><dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-148"><dt>**Ndis802\_11AuthModeWPA**</dt> <dt>4</dt></span></span> </dl>                             | <span data-ttu-id="8419e-149">Sécurité WPA (Wireless Protected Access).</span><span class="sxs-lookup"><span data-stu-id="8419e-149">Wireless Protected Access(WPA) security.</span></span> <span data-ttu-id="8419e-150">L’authentification est effectuée entre le demandeur, l’authentificateur et le serveur d’authentification sur IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="8419e-150">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="8419e-151">Les clés de chiffrement sont dynamiques et sont dérivées par le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8419e-151">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <span data-ttu-id="8419e-152"><dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-152"><dt>**Ndis802\_11AuthModeWPAPSK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="8419e-153">La sécurité WPA à l’aide d’une clé prépartagée.</span><span class="sxs-lookup"><span data-stu-id="8419e-153">WPA security using a pre-shared key.</span></span> <span data-ttu-id="8419e-154">L’authentification est effectuée entre le demandeur et l’authentificateur sur IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="8419e-154">Authentication is performed between the supplicant and authenticator over IEEE 802.1X.</span></span> <span data-ttu-id="8419e-155">Les clés de chiffrement sont dynamiques et sont dérivées de la clé prépartagée utilisée par le demandeur et l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="8419e-155">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <span data-ttu-id="8419e-156"><dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-156"><dt>**Ndis802\_11AuthModeWPANone**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="8419e-157">Sécurité WPA.</span><span class="sxs-lookup"><span data-stu-id="8419e-157">WPA security.</span></span> <span data-ttu-id="8419e-158">L’authentification s’effectue à l’aide d’une clé prépartagée sans authentification IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="8419e-158">Authentication is performed using a preshared key without IEEE 802.1X authentication.</span></span> <span data-ttu-id="8419e-159">Les clés de chiffrement sont statiques et sont dérivées de la clé prépartagée.</span><span class="sxs-lookup"><span data-stu-id="8419e-159">Encryption keys are static and are derived through the preshared key.</span></span> <span data-ttu-id="8419e-160">Ce mode s’applique uniquement aux types de réseau ad hoc.</span><span class="sxs-lookup"><span data-stu-id="8419e-160">This mode is applicable only to ad hoc network types.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <span data-ttu-id="8419e-161"><dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-161"><dt>**Ndis802\_11AuthModeWPA2**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="8419e-162">Sécurité WPA2.</span><span class="sxs-lookup"><span data-stu-id="8419e-162">WPA2 security.</span></span> <span data-ttu-id="8419e-163">L’authentification est effectuée entre le demandeur, l’authentificateur et le serveur d’authentification sur IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="8419e-163">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="8419e-164">Les clés de chiffrement sont dynamiques et sont dérivées par le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8419e-164">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <span data-ttu-id="8419e-165"><dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-165"><dt>**Ndis802\_11AuthModeWPA2PSK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="8419e-166">Spécifie la sécurité WPA2.</span><span class="sxs-lookup"><span data-stu-id="8419e-166">Specifies WPA2 security.</span></span> <span data-ttu-id="8419e-167">L’authentification est effectuée entre le demandeur et l’authentificateur sur IEEE 802 1X.</span><span class="sxs-lookup"><span data-stu-id="8419e-167">Authentication is performed between the supplicant and authenticator over IEEE 802 1X.</span></span> <span data-ttu-id="8419e-168">Les clés de chiffrement sont dynamiques et sont dérivées de la clé prépartagée utilisée par le demandeur et l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="8419e-168">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <span data-ttu-id="8419e-169"><dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-169"><dt>**Ndis802\_11AuthModeMax**</dt> <dt>9</dt></span></span> </dl>                             | <span data-ttu-id="8419e-170">Valeur maximale possible pour la valeur d’énumération du **\_ \_ \_ \_ mode d’authentification NDIS 802 11** .</span><span class="sxs-lookup"><span data-stu-id="8419e-170">The maximum possible value for the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration value.</span></span> <span data-ttu-id="8419e-171">Il ne s’agit pas d’une valeur légale pour le mode d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8419e-171">This is not a legal value for the authentication mode.</span></span> <br/>                                                                                        |



 

</dd> <dt>

<span data-ttu-id="8419e-172">**nWepStatus**</span><span class="sxs-lookup"><span data-stu-id="8419e-172">**nWepStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-173">Mode de chiffrement actuel 802,11 défini sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-173">The current 802.11 Encryption Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-174">**dwCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="8419e-174">**dwCtlFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-175">Valeur de masque de masque des indicateurs de contrôle qui indiquent la manière dont WZCSVC fonctionne sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-175">A bitmask value of control flags that indicate how WZCSVC is operating on the interface.</span></span>

<span data-ttu-id="8419e-176">Le tableau suivant indique les valeurs de bit possibles.</span><span class="sxs-lookup"><span data-stu-id="8419e-176">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="8419e-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="8419e-177">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="8419e-178">Signification</span><span class="sxs-lookup"><span data-stu-id="8419e-178">Meaning</span></span>                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <span data-ttu-id="8419e-179"><dt>**INTFCTL \_ 0x0007 \_ masque de cm**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8419e-179"><dt>**INTFCTL\_CM\_MASK**</dt> <dt>0x0007</dt></span></span> </dl>      | <span data-ttu-id="8419e-180">Masque de masque pour le mode de filtre réseau.</span><span class="sxs-lookup"><span data-stu-id="8419e-180">A bitmask for the network filter mode.</span></span> <span data-ttu-id="8419e-181">INTFCTL \_ cm \_ Mask & dwCtlFlags génère une valeur de type NDIS \_ 802 \_ 11 \_ \_ infrastructure réseau.</span><span class="sxs-lookup"><span data-stu-id="8419e-181">INTFCTL\_CM\_MASK & dwCtlFlags result in a value of the type NDIS\_802\_11\_NETWORK\_INFRASTRUCTURE.</span></span> <span data-ttu-id="8419e-182">La valeur obtenue indique si WZCSVC se connecte uniquement aux réseaux d’infrastructure, aux réseaux ad hoc ou aux deux types de réseaux.</span><span class="sxs-lookup"><span data-stu-id="8419e-182">The resulting value indicates whether WZCSVC connects only to infrastructure networks, adhoc networks, or to both types of networks.</span></span><br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <span data-ttu-id="8419e-183"><dt>**INTFCTL \_ ACTIVÉ**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-183"><dt>**INTFCTL\_ENABLED**</dt> <dt>0x8000</dt></span></span> </dl>       | <span data-ttu-id="8419e-184">Indique si WZCSVC doit configurer l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-184">Indicates whether WZCSVC should configure the interface.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <span data-ttu-id="8419e-185"><dt>**INTFCTL \_**</dt> <dt>0X4000</dt> de secours</span><span class="sxs-lookup"><span data-stu-id="8419e-185"><dt>**INTFCTL\_FALLBACK**</dt> <dt>0x4000</dt></span></span> </dl>    | <span data-ttu-id="8419e-186">Si un réseau préféré n’est pas disponible, cette valeur indique si la configuration de la carte réseau doit être automatiquement configurée pour s’associer à un réseau disponible.</span><span class="sxs-lookup"><span data-stu-id="8419e-186">If a preferred network is not available, this value indicates whether WZCSVC should automatically configure the NIC to associate to any available network.</span></span><br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <span data-ttu-id="8419e-187"><dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-187"><dt>**INTFCTL\_OIDSSUPP** </dt> <dt>0x2000</dt></span></span> </dl> | <span data-ttu-id="8419e-188">Indique si le pilote de carte réseau prend en charge tous les 802,11 OID requis par WZCSVC pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="8419e-188">Indicates whether the NIC driver supports all the 802.11 OIDs required by WZCSVC to function.</span></span><br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <span data-ttu-id="8419e-189"><dt> **INTFCTL \_ volatile**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-189"><dt>**INTFCTL\_VOLATILE** </dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="8419e-190">Indique si les paramètres de service de cette interface doivent être conservés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8419e-190">Indicates whether the service parameters for this interface should be retained in the registry.</span></span> <br/> <span data-ttu-id="8419e-191">Si cette valeur est définie, ces paramètres sont volatiles et ne doivent pas être conservés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8419e-191">If this value is set, then these parameters are volatile and should not be retained in the registry.</span></span><br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <span data-ttu-id="8419e-192"><dt> **\_ Stratégie INTFCTL**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-192"><dt>**INTFCTL\_POLICY** </dt> <dt>0x0800</dt></span></span> </dl>       | <span data-ttu-id="8419e-193">Indique si les paramètres de service pour cette interface font l’objet d’un push par une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8419e-193">Indicates whether the service parameters for this interface are pushed by a group policy.</span></span><br/> <span data-ttu-id="8419e-194">Si cette valeur est définie, les paramètres du service sont envoyés à l’ordinateur local par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8419e-194">If this value is set, then the service parameters are pushed to the local computer by group policy.</span></span><br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <span data-ttu-id="8419e-195"><dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-195"><dt>**INTFCTL\_8021XSUPP**</dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="8419e-196">Indique si la prise en charge de 802.1 X est activée.</span><span class="sxs-lookup"><span data-stu-id="8419e-196">Indicates whether 802.1X support is enabled.</span></span><br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="8419e-197">**dwDynFlags**</span><span class="sxs-lookup"><span data-stu-id="8419e-197">**dwDynFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-198">Masque de bits des indicateurs dynamiques qui contrôlent le comportement dynamique (non persistant et non statique) sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-198">A bitmask of dynamic flags that control the dynamic (non-persistent and non-static) behavior on the interface.</span></span>

<span data-ttu-id="8419e-199">Ces bits sont utiles pour déclencher des modifications dynamiques et temporaires dans la façon dont le WZCSVC agit sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-199">These bits are useful to trigger dynamic, temporary changes in the way the WZCSVC acts on the interface.</span></span> <span data-ttu-id="8419e-200">Aucun de ces bits n’étant conservé dans le registre, les paramètres ne survivront pas au redémarrage du système ou à la désactivation de l’appareil et à l’activation de la séquence.</span><span class="sxs-lookup"><span data-stu-id="8419e-200">None of these bits are persisted in the registry, so the settings won't survive a system restart or a device disable and enable sequence.</span></span>

<span data-ttu-id="8419e-201">Le tableau suivant indique les valeurs de bit possibles.</span><span class="sxs-lookup"><span data-stu-id="8419e-201">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="8419e-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="8419e-202">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="8419e-203">Signification</span><span class="sxs-lookup"><span data-stu-id="8419e-203">Meaning</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <span data-ttu-id="8419e-204"><dt>**INTFDYN \_ Noscan**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-204"><dt>**INTFDYN\_NOSCAN**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="8419e-205">Indique que le WZCSVC ne doit pas demander que l’interface exécute une analyse active, mais utilise à la place les valeurs mises en cache dans le pilote de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="8419e-205">Indicates that the WZCSVC should not request the interface conduct an active scan, but instead use the cached values in the NIC driver.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8419e-206">**dwCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8419e-206">**dwCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-207">Spécifie les fonctionnalités du pilote.</span><span class="sxs-lookup"><span data-stu-id="8419e-207">Specifies the driver capabilities.</span></span>



| <span data-ttu-id="8419e-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="8419e-208">Value</span></span>                                                                                                                                                                                                                                                         | <span data-ttu-id="8419e-209">Signification</span><span class="sxs-lookup"><span data-stu-id="8419e-209">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <span data-ttu-id="8419e-210"><dt>**INTFCAP \_ 0x000000FF \_ \_ masque de CHIFFREment Max**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8419e-210"><dt>**INTFCAP\_MAX\_CIPHER\_MASK**</dt> <dt>0x000000ff</dt></span></span> </dl> | <span data-ttu-id="8419e-211">Les bits d’ordre inférieur de ce membre sont utilisés pour indiquer le chiffrement maximal pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8419e-211">The lower order bits of this member are used to indicate the maximum encryption that is supported.</span></span> <span data-ttu-id="8419e-212">Les valeurs possibles sont certaines des valeurs d’énumération définies dans la structure d' **\_ état NDIS 802 \_ 11 \_ WEP \_** dans le fichier d’en-tête *NtDDNdis. h* inclus dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8419e-212">The possible values are some of the enumeration values defined in the **NDIS\_802\_11\_WEP\_STATUS** structure in the *NtDDNdis.h* header file included in the Windows SDK.</span></span><br/> <span data-ttu-id="8419e-213">La \_ valeur Ndis802 11Encryption1Enabled (2) indique que le chiffrement WEP est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8419e-213">The Ndis802\_11Encryption1Enabled value (2) indicates that WEP is supported.</span></span> <span data-ttu-id="8419e-214">TKIP et AES ne sont pas pris en charge, et une clé de transmission peut être ou non disponible.</span><span class="sxs-lookup"><span data-stu-id="8419e-214">TKIP and AES are not supported, and a transmit key may or may not be available.</span></span> <br/> <span data-ttu-id="8419e-215">La \_ valeur Ndis802 11Encryption2Enabled (9) indique que le protocole TKIP et le chiffrement WEP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8419e-215">The Ndis802\_11Encryption2Enabled value (9) indicates that TKIP and WEP are supported.</span></span> <span data-ttu-id="8419e-216">AES n’est pas pris en charge et une clé de transmission est disponible.</span><span class="sxs-lookup"><span data-stu-id="8419e-216">AES is not supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="8419e-217">La \_ valeur de 11Encryption3Enabled Ndis802 (11) indique que AES, TKIP et WEP sont pris en charge, et une clé de transmission est disponible.</span><span class="sxs-lookup"><span data-stu-id="8419e-217">The Ndis802\_11Encryption3Enabled value (11) indicates that AES, TKIP, and WEP are supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="8419e-218">Le Ndis802 \_ 11EncryptionNotSupported (8) indique que la clé WEP n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8419e-218">The Ndis802\_11EncryptionNotSupported (8) indicates Indicates that the WEP key is not supported.</span></span> <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <span data-ttu-id="8419e-219"><dt>**INTFCAP \_**</dt> <dt>0x00000100</dt> SSN</span><span class="sxs-lookup"><span data-stu-id="8419e-219"><dt>**INTFCAP\_SSN**</dt> <dt>0x00000100</dt></span></span> </dl>                                       | <span data-ttu-id="8419e-220">Indique la prise en charge d’un réseau sécurisé simple (SSN) qui est un sous-ensemble de 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="8419e-220">Indicates support for Simple Secure Network (SSN) which is a subset of 802.11i.</span></span> <br/> <span data-ttu-id="8419e-221">SSN modifie régulièrement la clé de chiffrement, au lieu de la norme WEP (Wired Equivalent Privacy), qui utilise une clé statique.</span><span class="sxs-lookup"><span data-stu-id="8419e-221">SSN changes the encryption key periodically, as opposed to the WEP (Wired Equivalent Privacy) standard, which uses a static key.</span></span> <span data-ttu-id="8419e-222">Pour que SSN fonctionne, le chiffrement maximal pris en charge doit être au moins TKIP.</span><span class="sxs-lookup"><span data-stu-id="8419e-222">In order for SSN to work, the maximum supported cipher should be at least TKIP.</span></span> <span data-ttu-id="8419e-223">Le numéro de sécurité sociale a été développé par un consortium de fournisseurs dans 2002 en tant qu’approche temporaire pour améliorer la sécurité des réseaux locaux sans fil pendant la réalisation de la norme IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="8419e-223">SSN was developed by a consortium of vendors in 2002 as an interim approach to improve wireless LAN security while the IEEE 802.11i standard was being completed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <span data-ttu-id="8419e-224"><dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-224"><dt>**INTFCAP\_80211I**</dt> <dt>0x00000200</dt></span></span> </dl>                              | <span data-ttu-id="8419e-225">Indique la prise en charge de la norme IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="8419e-225">Indicates support for the IEEE 802.11i standard.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="8419e-226">**rdNicCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8419e-226">**rdNicCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-227">Ensemble de fonctionnalités pour 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="8419e-227">A set of capabilities for 802.11i.</span></span>

<span data-ttu-id="8419e-228">La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdNicCapabilities** quand elles sont appelées avec l’indicateur de **\_ fonctionnalités INTF** passé dans le paramètre *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="8419e-228">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdNicCapabilities** data when called with the **INTF\_CAPABILITIES** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="8419e-229">Si l’appel de fonction réussit, le membre **pData** de la structure de **\_ données brutes** contient une structure de **\_ \_ capacité INTF 80211** .</span><span class="sxs-lookup"><span data-stu-id="8419e-229">If the function call is successful, the **pData** member of the **RAW\_DATA** structure contains an **INTF\_80211\_CAPABILITY** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-230">**rdSSID**</span><span class="sxs-lookup"><span data-stu-id="8419e-230">**rdSSID**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-231">Données binaires contenant le SSID 802,11 actuellement configuré sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-231">Binary data containing the 802.11 SSID currently configured on the interface.</span></span>

<span data-ttu-id="8419e-232">La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdSSID** quand elles sont appelées avec l’indicateur **\_ SSID INTF** passé dans le paramètre *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="8419e-232">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdSSID** data when called with the **INTF\_SSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="8419e-233">Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient le membre **SsidLength** d’une structure de **\_ SSID NDIS 802 \_ \_ 11** et le membre **pData** de la structure de **\_ données brutes** contient le membre **SSID** d’une structure **NDIS \_ 802 \_ 11 \_ SSID** .</span><span class="sxs-lookup"><span data-stu-id="8419e-233">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the **SsidLength** member of a **NDIS\_802\_11\_SSID** structure and the **pData** member of the **RAW\_DATA** structure contains the **Ssid** member of a **NDIS\_802\_11\_SSID** structure.</span></span>

<span data-ttu-id="8419e-234">La structure du **\_ \_ \_ SSID NDIS 802 11** est définie dans le fichier d’en-tête *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="8419e-234">The **NDIS\_802\_11\_SSID** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-235">**rdBSSID**</span><span class="sxs-lookup"><span data-stu-id="8419e-235">**rdBSSID**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-236">Données binaires contenant l' 802,11 BSSID configuré sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-236">Binary data containing the 802.11 BSSID configured on the interface.</span></span>

<span data-ttu-id="8419e-237">La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdBSSID** quand elles sont appelées avec l’indicateur **INTF \_ BSSID** passé dans le paramètre *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="8419e-237">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSID** data when called with the **INTF\_BSSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="8419e-238">Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient la taille d’une structure d' **\_ \_ \_ \_ adresse Mac NDIS 802 11** et le membre **pData** de la structure de **\_ données brutes** contient la structure d' **\_ \_ \_ \_ adresse Mac NDIS 802 11** .</span><span class="sxs-lookup"><span data-stu-id="8419e-238">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the size of an **NDIS\_802\_11\_MAC\_ADDRESS** structure and the **pData** member of the **RAW\_DATA** structure contains the **NDIS\_802\_11\_MAC\_ADDRESS** structure.</span></span>

<span data-ttu-id="8419e-239">La structure d' **\_ \_ \_ \_ adresse Mac NDIS 802 11** est définie dans le fichier d’en-tête *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="8419e-239">The **NDIS\_802\_11\_MAC\_ADDRESS** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-240">**rdBSSIDList**</span><span class="sxs-lookup"><span data-stu-id="8419e-240">**rdBSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-241">Données binaires qui contiennent la liste des BSSIDs qui ont été récupérées pour la dernière fois par WZCSVC.</span><span class="sxs-lookup"><span data-stu-id="8419e-241">Binary data that contains the list of BSSIDs that was last retrieved by WZCSVC.</span></span>

<span data-ttu-id="8419e-242">La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdBSSIDList** quand elles sont appelées avec l’indicateur **INTF \_ BSSIDLIST** passé dans le paramètre *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="8419e-242">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSIDList** data when called with the **INTF\_BSSIDLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="8419e-243">Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient la longueur de la mémoire tampon avec les données retournées et le membre **PData** de la structure de **\_ données brutes** contient la structure de liste de **\_ configuration WZC 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="8419e-243">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-244">**rdStSSIDList**</span><span class="sxs-lookup"><span data-stu-id="8419e-244">**rdStSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-245">Données binaires qui contiennent la liste des réseaux préférés configurés pour cette interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-245">Binary data that contains the list of preferred networks configured for this interface.</span></span>

<span data-ttu-id="8419e-246">La fonction [**WZCQueryInterface**](wzcqueryinterface.md) retourne les données **rdStSSIDList** quand elles sont appelées avec l’indicateur **INTF \_ PREFLIST** passé dans le paramètre *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="8419e-246">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdStSSIDList** data when called with the **INTF\_PREFLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="8419e-247">Si l’appel de fonction réussit, le membre **dwDataLen** de la structure de **\_ données brutes** contient la longueur de la mémoire tampon avec les données retournées et le membre **PData** de la structure de **\_ données brutes** contient la structure de liste de **\_ configuration WZC 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="8419e-247">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

<span data-ttu-id="8419e-248">Si l’un des réseaux préférés est actuellement connecté, le jeu de bits **WZCCTL \_ Media \_ Connected** (0x0400) est défini pour le membre **dwCtlFlags** de la structure de **\_ \_ configuration WLAN WZC** pour le réseau.</span><span class="sxs-lookup"><span data-stu-id="8419e-248">If one of the preferred networks is currently connected, the **dwCtlFlags** member of the **WZC\_WLAN\_CONFIG** structure for the network will have the **WZCCTL\_MEDIA\_CONNECTED** (0x0400) bit set.</span></span>

</dd> <dt>

<span data-ttu-id="8419e-249">**rdCtrlData**</span><span class="sxs-lookup"><span data-stu-id="8419e-249">**rdCtrlData**</span></span>
</dt> <dd>

<span data-ttu-id="8419e-250">Données binaires utilisées avec d’autres indicateurs de contrôle lors de la définition de paramètres supplémentaires sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="8419e-250">Binary data used with other control flags, when setting additional parameters on the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8419e-251">Notes</span><span class="sxs-lookup"><span data-stu-id="8419e-251">Remarks</span></span>

<span data-ttu-id="8419e-252">La structure d' **\_ entrée INTF** est utilisée par les fonctions [**WZCQueryInterface**](wzcqueryinterface.md) et [**WZCRefreshInterface**](wzcrefreshinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="8419e-252">The **INTF\_ENTRY** structure is used by the [**WZCQueryInterface**](wzcqueryinterface.md) and [**WZCRefreshInterface**](wzcrefreshinterface.md) functions.</span></span>

<span data-ttu-id="8419e-253">La structure des **\_ données brutes** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="8419e-253">The **RAW\_DATA** structure is defined as follows:</span></span>


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



<span data-ttu-id="8419e-254">Le membre *pData* pointe vers les données binaires.</span><span class="sxs-lookup"><span data-stu-id="8419e-254">The *pData* member points to binary data.</span></span> <span data-ttu-id="8419e-255">*DwDataLen* indique le nombre d’octets pointés par *pData*.</span><span class="sxs-lookup"><span data-stu-id="8419e-255">The *dwDataLen* indicates the number of bytes pointed by *pData*.</span></span>

> [!Note]  
> <span data-ttu-id="8419e-256">Le fichier d’en-tête *wzcsapi. h* n’est pas disponible dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8419e-256">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8419e-257">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8419e-257">Requirements</span></span>



| <span data-ttu-id="8419e-258">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8419e-258">Requirement</span></span> | <span data-ttu-id="8419e-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="8419e-259">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8419e-260">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8419e-260">Minimum supported client</span></span><br/> | <span data-ttu-id="8419e-261">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8419e-261">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8419e-262">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8419e-262">Minimum supported server</span></span><br/> | <span data-ttu-id="8419e-263">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8419e-263">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8419e-264">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8419e-264">End of client support</span></span><br/>    | <span data-ttu-id="8419e-265">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="8419e-265">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="8419e-266">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8419e-266">End of server support</span></span><br/>    | <span data-ttu-id="8419e-267">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8419e-267">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8419e-268">En-tête</span><span class="sxs-lookup"><span data-stu-id="8419e-268">Header</span></span><br/>                   | <dl> <span data-ttu-id="8419e-269"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8419e-269"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8419e-270">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8419e-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8419e-271">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="8419e-271">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="8419e-272">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="8419e-272">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="8419e-273">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="8419e-273">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 




