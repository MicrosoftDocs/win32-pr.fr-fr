---
title: Classe MDM_VPNv2_CryptographySuite03
description: La \_ classe VPNv2 \_ CryptographySuite03 MDM contient des informations de chiffrement pour le profil VPN natif.
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- Classe MDM_VPNv2_CryptographySuite03
- Classe MDM_VPNv2_CryptographySuite03, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465343"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a><span data-ttu-id="3c5f6-105">\_ \_ Classe CRYPTOGRAPHYSUITE03 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="3c5f6-105">MDM\_VPNv2\_CryptographySuite03 class</span></span>

<span data-ttu-id="3c5f6-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="3c5f6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3c5f6-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="3c5f6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3c5f6-108">La **classe \_ VPNv2 \_ CryptographySuite03 MDM** contient des informations de chiffrement pour le profil VPN natif.</span><span class="sxs-lookup"><span data-stu-id="3c5f6-108">The **MDM\_VPNv2\_CryptographySuite03** class contains cryptography information for the native VPN profile.</span></span>

<span data-ttu-id="3c5f6-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3c5f6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c5f6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c5f6-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a><span data-ttu-id="3c5f6-111">Membres</span><span class="sxs-lookup"><span data-stu-id="3c5f6-111">Members</span></span>

<span data-ttu-id="3c5f6-112">La **classe \_ VPNv2 \_ CryptographySuite03 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3c5f6-112">The **MDM\_VPNv2\_CryptographySuite03** class has these types of members:</span></span>

-   [<span data-ttu-id="3c5f6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c5f6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c5f6-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c5f6-114">Properties</span></span>

<span data-ttu-id="3c5f6-115">La **classe \_ VPNv2 \_ CryptographySuite03 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c5f6-115">The **MDM\_VPNv2\_CryptographySuite03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3c5f6-116">AuthenticationTransformConstants</span><span class="sxs-lookup"><span data-stu-id="3c5f6-116">AuthenticationTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c5f6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5f6-119">CipherTransformConstants</span><span class="sxs-lookup"><span data-stu-id="3c5f6-119">CipherTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c5f6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5f6-122">DHGroup</span><span class="sxs-lookup"><span data-stu-id="3c5f6-122">DHGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c5f6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c5f6-125">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="3c5f6-125">EncryptionMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c5f6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c5f6-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c5f6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c5f6-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c5f6-132">Nœud contenant les propriétés des tunnels IPSec.</span><span class="sxs-lookup"><span data-stu-id="3c5f6-132">Node containing the properties of IPSec tunnels.</span></span>

</dd> <dt>

[<span data-ttu-id="3c5f6-133">IntegrityCheckMethod</span><span class="sxs-lookup"><span data-stu-id="3c5f6-133">IntegrityCheckMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c5f6-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c5f6-136">**ID**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c5f6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-139">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c5f6-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c5f6-140">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="3c5f6-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="3c5f6-141">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile »</span><span class="sxs-lookup"><span data-stu-id="3c5f6-141">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="3c5f6-142">PfsGroup</span><span class="sxs-lookup"><span data-stu-id="3c5f6-142">PfsGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c5f6-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c5f6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c5f6-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c5f6-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c5f6-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c5f6-145">Requirements</span></span>



| <span data-ttu-id="3c5f6-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c5f6-146">Requirement</span></span> | <span data-ttu-id="3c5f6-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c5f6-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5f6-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c5f6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5f6-149">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c5f6-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c5f6-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c5f6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5f6-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c5f6-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3c5f6-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c5f6-152">Namespace</span></span><br/>                | <span data-ttu-id="3c5f6-153">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3c5f6-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3c5f6-154">MOF</span><span class="sxs-lookup"><span data-stu-id="3c5f6-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c5f6-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c5f6-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c5f6-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3c5f6-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c5f6-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c5f6-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

