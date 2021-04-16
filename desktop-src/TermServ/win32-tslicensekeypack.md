---
title: Classe Win32_TSLicenseKeyPack
description: Fournit des méthodes et des propriétés pour l’affichage et l’installation de Services Bureau à distance les jeux de clés de licence.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508325"
---
# <a name="win32_tslicensekeypack-class"></a><span data-ttu-id="f4136-105">\_Classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="f4136-105">Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="f4136-106">Fournit des méthodes et des propriétés pour l’affichage et l’installation de Services Bureau à distance les jeux de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="f4136-106">Provides methods and properties for viewing and installing Remote Desktop Services license key packs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4136-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4136-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a><span data-ttu-id="f4136-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f4136-108">Members</span></span>

<span data-ttu-id="f4136-109">La classe **Win32 \_ TSLicenseKeyPack** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f4136-109">The **Win32\_TSLicenseKeyPack** class has these types of members:</span></span>

-   [<span data-ttu-id="f4136-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f4136-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f4136-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4136-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f4136-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f4136-112">Methods</span></span>

<span data-ttu-id="f4136-113">La classe **Win32 \_ TSLicenseKeyPack** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f4136-113">The **Win32\_TSLicenseKeyPack** class has these methods.</span></span>



| <span data-ttu-id="f4136-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="f4136-114">Method</span></span>                                                                                                        | <span data-ttu-id="f4136-115">Description</span><span class="sxs-lookup"><span data-stu-id="f4136-115">Description</span></span>                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4136-116">**ConvertLicenses**</span><span class="sxs-lookup"><span data-stu-id="f4136-116">**ConvertLicenses**</span></span>](convertlicenses-win32-tslicensekeypack.md)                                             | <span data-ttu-id="f4136-117">Convertit les licences dans le jeu de clés actuel.</span><span class="sxs-lookup"><span data-stu-id="f4136-117">Converts the licenses in the current key pack.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="f4136-118">**ImportAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-118">**ImportAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | <span data-ttu-id="f4136-119">Les importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.</span><span class="sxs-lookup"><span data-stu-id="f4136-119">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/> |
| [<span data-ttu-id="f4136-120">**ImportLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="f4136-120">**ImportLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | <span data-ttu-id="f4136-121">Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance qui utilise un identificateur de licence reçu via Internet ou le téléphone.</span><span class="sxs-lookup"><span data-stu-id="f4136-121">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span><br/>                                               |
| [<span data-ttu-id="f4136-122">**ImportOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-122">**ImportOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | <span data-ttu-id="f4136-123">Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Open License Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-123">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="f4136-124">**ImportRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-124">**ImportRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | <span data-ttu-id="f4136-125">Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="f4136-125">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                   |
| [<span data-ttu-id="f4136-126">**InstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-126">**InstallAgreementLicenseKeyPack**</span></span>](installagreementlicensekeypack-win32-tslicensekeypack.md)               | <span data-ttu-id="f4136-127">Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’une licence de contrat.</span><span class="sxs-lookup"><span data-stu-id="f4136-127">Installs a Remote Desktop Services license key pack that was purchased through an agreement license.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="f4136-128">**InstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-128">**InstallLicenseKeyPack**</span></span>](installlicensekeypack-win32-tslicensekeypack.md)                                 | <span data-ttu-id="f4136-129">Installe un jeu de clés de licence Services Bureau à distance qui utilise un ID de jeu de clés de licence reçu via Internet ou par téléphone.</span><span class="sxs-lookup"><span data-stu-id="f4136-129">Installs a Remote Desktop Services license key pack that uses a license key pack ID that was received over the Internet or the phone.</span></span><br/>                                                                                          |
| [<span data-ttu-id="f4136-130">**InstallOpenLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-130">**InstallOpenLicenseKeyPack**</span></span>](installopenlicensekeypack-win32-tslicensekeypack.md)                         | <span data-ttu-id="f4136-131">Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence ouvert.</span><span class="sxs-lookup"><span data-stu-id="f4136-131">Installs a Remote Desktop Services license key pack that was purchased through an open license agreement.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="f4136-132">**InstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-132">**InstallRetailPurchaseLicenseKeyPack**</span></span>](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | <span data-ttu-id="f4136-133">Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un magasin de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="f4136-133">Installs a Remote Desktop Services license key pack that was purchased through a retail store.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="f4136-134">**ReinstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-134">**ReinstallAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | <span data-ttu-id="f4136-135">Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.</span><span class="sxs-lookup"><span data-stu-id="f4136-135">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/>                                           |
| [<span data-ttu-id="f4136-136">**ReinstallLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="f4136-136">**ReinstallLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | <span data-ttu-id="f4136-137">Réinstalle un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu sur Internet ou sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="f4136-137">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f4136-138">**ReinstallOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-138">**ReinstallOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | <span data-ttu-id="f4136-139">Réinstalle un jeu de clés de licence Open License Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-139">Reinstalls an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="f4136-140">**ReinstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-140">**ReinstallRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | <span data-ttu-id="f4136-141">Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="f4136-141">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="f4136-142">**RemoveLicensesWithIdCount**</span><span class="sxs-lookup"><span data-stu-id="f4136-142">**RemoveLicensesWithIdCount**</span></span>](win32-tslicensekeypack-removelicenseswithidcount.md)                         | <span data-ttu-id="f4136-143">Supprime le nombre spécifié de licences Services Bureau à distance du jeu de clés spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4136-143">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="f4136-144">**UninstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f4136-144">**UninstallLicenseKeyPack**</span></span>](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | <span data-ttu-id="f4136-145">Désinstalle un jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-145">Uninstalls a Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="f4136-146">**UninstallLicenseKeyPackWithId**</span><span class="sxs-lookup"><span data-stu-id="f4136-146">**UninstallLicenseKeyPackWithId**</span></span>](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | <span data-ttu-id="f4136-147">Désinstalle le jeu de clés de licence Services Bureau à distance avec l’identificateur de package de clés spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4136-147">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="f4136-148">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4136-148">Properties</span></span>

<span data-ttu-id="f4136-149">La classe **Win32 \_ TSLicenseKeyPack** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f4136-149">The **Win32\_TSLicenseKeyPack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4136-150">**AccessRights**</span><span class="sxs-lookup"><span data-stu-id="f4136-150">**AccessRights**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4136-153">Qualificateurs : [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) (« 0 », « 1 », « 2 », « 3 »), [**bitvalues**](/windows/desktop/WmiSdk/standard-qualifiers) (« session Rd », « session VDI », « Calista », « partenaires VDI »)</span><span class="sxs-lookup"><span data-stu-id="f4136-153">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calista", "VDI Partners")</span></span>
</dt> </dl>

<span data-ttu-id="f4136-154">Qualificateur pour les droits d’accès au Pack de clés du gestionnaire de licences TS</span><span class="sxs-lookup"><span data-stu-id="f4136-154">Qualifier for TS Licensing key pack access rights</span></span>

</dd> <dt>

<span data-ttu-id="f4136-155">**AvailableLicenses**</span><span class="sxs-lookup"><span data-stu-id="f4136-155">**AvailableLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-156">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-158">Nombre total de licences disponibles dans le jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-158">Total number of available licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="f4136-159">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4136-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4136-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-162">Description du jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-162">Description of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="f4136-163">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="f4136-163">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-164">Type de données : **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="f4136-164">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-166">Date d’expiration du jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-166">The expiration date of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="f4136-167">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="f4136-167">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-170">Nombre total de licences émises dans le jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-170">Total number of issued licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="f4136-171">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="f4136-171">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4136-174">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f4136-174">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f4136-175">Identificateur du jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-175">Identifier for the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="f4136-176">**KeyPackType**</span><span class="sxs-lookup"><span data-stu-id="f4136-176">**KeyPackType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-179">Type de jeu de clés pour le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-179">Type of key pack for the Remote Desktop license server.</span></span>

| <span data-ttu-id="f4136-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4136-180">Value</span></span> | <span data-ttu-id="f4136-181">Description</span><span class="sxs-lookup"><span data-stu-id="f4136-181">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f4136-182">0</span><span class="sxs-lookup"><span data-stu-id="f4136-182">0</span></span> | <span data-ttu-id="f4136-183">Le type de jeu de clés de licence Services Bureau à distance est inconnu.</span><span class="sxs-lookup"><span data-stu-id="f4136-183">The Remote Desktop Services license key pack type is unknown.</span></span> |
| <span data-ttu-id="f4136-184">1</span><span class="sxs-lookup"><span data-stu-id="f4136-184">1</span></span> | <span data-ttu-id="f4136-185">Le type de jeu de clés de licence Services Bureau à distance est un achat au détail.</span><span class="sxs-lookup"><span data-stu-id="f4136-185">The Remote Desktop Services license key pack type is a retail purchase.</span></span> |
| <span data-ttu-id="f4136-186">2</span><span class="sxs-lookup"><span data-stu-id="f4136-186">2</span></span> | <span data-ttu-id="f4136-187">Le type de jeu de clés de licence Services Bureau à distance est un achat en volume.</span><span class="sxs-lookup"><span data-stu-id="f4136-187">The Remote Desktop Services license key pack type is a volume purchase.</span></span> |
| <span data-ttu-id="f4136-188">3</span><span class="sxs-lookup"><span data-stu-id="f4136-188">3</span></span> | <span data-ttu-id="f4136-189">Le type de jeu de clés de licence Services Bureau à distance est une licence simultanée.</span><span class="sxs-lookup"><span data-stu-id="f4136-189">The Remote Desktop Services license key pack type is a concurrent license.</span></span> |
| <span data-ttu-id="f4136-190">4</span><span class="sxs-lookup"><span data-stu-id="f4136-190">4</span></span> | <span data-ttu-id="f4136-191">Le type de jeu de clés de licence Services Bureau à distance est temporaire.</span><span class="sxs-lookup"><span data-stu-id="f4136-191">The Remote Desktop Services license key pack type is temporary.</span></span> |
| <span data-ttu-id="f4136-192">5</span><span class="sxs-lookup"><span data-stu-id="f4136-192">5</span></span> | <span data-ttu-id="f4136-193">Le type de jeu de clés de licence Services Bureau à distance est une licence ouverte.</span><span class="sxs-lookup"><span data-stu-id="f4136-193">The Remote Desktop Services license key pack type is an open license.</span></span> |
| <span data-ttu-id="f4136-194">6</span><span class="sxs-lookup"><span data-stu-id="f4136-194">6</span></span> | <span data-ttu-id="f4136-195">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f4136-195">Not supported.</span></span> |

<span data-ttu-id="f4136-196">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="f4136-196">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-199">Type de produit du jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-199">Product type of the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="f4136-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4136-200">Value</span></span> | <span data-ttu-id="f4136-201">Description</span><span class="sxs-lookup"><span data-stu-id="f4136-201">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f4136-202">0</span><span class="sxs-lookup"><span data-stu-id="f4136-202">0</span></span> | <span data-ttu-id="f4136-203">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="f4136-203">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="f4136-204">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="f4136-204">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="f4136-205">1</span><span class="sxs-lookup"><span data-stu-id="f4136-205">1</span></span> | <span data-ttu-id="f4136-206">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4136-206">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="f4136-207">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="f4136-207">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="f4136-208">2</span><span class="sxs-lookup"><span data-stu-id="f4136-208">2</span></span> | <span data-ttu-id="f4136-209">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f4136-209">This product type is not valid.</span></span> |

<span data-ttu-id="f4136-210">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="f4136-210">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4136-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-213">Version du produit pour le jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-213">Product version for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="f4136-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4136-214">Value</span></span> | <span data-ttu-id="f4136-215">Description</span><span class="sxs-lookup"><span data-stu-id="f4136-215">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f4136-216">« Windows Server 2012 »</span><span class="sxs-lookup"><span data-stu-id="f4136-216">"Windows Server 2012"</span></span> | <span data-ttu-id="f4136-217">Seuls les serveurs exécutant Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="f4136-217">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="f4136-218">« Windows Server 7 »</span><span class="sxs-lookup"><span data-stu-id="f4136-218">"Windows Server 7"</span></span> | <span data-ttu-id="f4136-219">Seuls les serveurs exécutant Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="f4136-219">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="f4136-220">« Windows Server 2008 »</span><span class="sxs-lookup"><span data-stu-id="f4136-220">"Windows Server 2008"</span></span> | <span data-ttu-id="f4136-221">Seuls les serveurs exécutant Windows Server 2008 sont pris en charge par ce pack de clés.</span><span class="sxs-lookup"><span data-stu-id="f4136-221">Only servers running Windows Server 2008 are supported by this key pack.</span></span> |

<span data-ttu-id="f4136-222">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="f4136-222">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-223">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-225">Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="f4136-225">Product version identifier for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="f4136-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4136-226">Value</span></span> | <span data-ttu-id="f4136-227">Description</span><span class="sxs-lookup"><span data-stu-id="f4136-227">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f4136-228">0</span><span class="sxs-lookup"><span data-stu-id="f4136-228">0</span></span> | <span data-ttu-id="f4136-229">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4136-229">Not supported</span></span> |
| <span data-ttu-id="f4136-230">1</span><span class="sxs-lookup"><span data-stu-id="f4136-230">1</span></span> | <span data-ttu-id="f4136-231">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4136-231">Not supported</span></span> |
| <span data-ttu-id="f4136-232">2</span><span class="sxs-lookup"><span data-stu-id="f4136-232">2</span></span> | <span data-ttu-id="f4136-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4136-233">Windows Server 2008</span></span> |
| <span data-ttu-id="f4136-234">3</span><span class="sxs-lookup"><span data-stu-id="f4136-234">3</span></span> | <span data-ttu-id="f4136-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4136-235">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="f4136-236">4</span><span class="sxs-lookup"><span data-stu-id="f4136-236">4</span></span> | <span data-ttu-id="f4136-237">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f4136-237">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="f4136-238">5</span><span class="sxs-lookup"><span data-stu-id="f4136-238">5</span></span> | <span data-ttu-id="f4136-239">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f4136-239">Windows Server 2016</span></span> |
| <span data-ttu-id="f4136-240">6</span><span class="sxs-lookup"><span data-stu-id="f4136-240">6</span></span> | <span data-ttu-id="f4136-241">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="f4136-241">Windows Server 2019</span></span> |

<span data-ttu-id="f4136-242">**TotalLicenses**</span><span class="sxs-lookup"><span data-stu-id="f4136-242">**TotalLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-243">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4136-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-245">Nombre total de licences dans le jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f4136-245">Total number of licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="f4136-246">**TypeAndModel**</span><span class="sxs-lookup"><span data-stu-id="f4136-246">**TypeAndModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4136-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4136-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4136-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4136-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4136-249">Qualificateur pour le type et le modèle de jeu de clés du gestionnaire de licences TS.</span><span class="sxs-lookup"><span data-stu-id="f4136-249">Qualifier for TS Licensing key pack type and model.</span></span> <span data-ttu-id="f4136-250">Exemples : licence d’abonnement VDI par appareil, CAL TS par utilisateur</span><span class="sxs-lookup"><span data-stu-id="f4136-250">Examples: VDI Per Device subscription license, TS Per User CAL</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4136-251">Notes</span><span class="sxs-lookup"><span data-stu-id="f4136-251">Remarks</span></span>

<span data-ttu-id="f4136-252">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="f4136-252">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="f4136-253">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f4136-253">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f4136-254">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f4136-254">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f4136-255">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f4136-255">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f4136-256">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f4136-256">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4136-257">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4136-257">Requirements</span></span>



| <span data-ttu-id="f4136-258">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4136-258">Requirement</span></span> | <span data-ttu-id="f4136-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4136-259">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4136-260">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4136-260">Minimum supported client</span></span><br/> | <span data-ttu-id="f4136-261">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4136-261">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f4136-262">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4136-262">Minimum supported server</span></span><br/> | <span data-ttu-id="f4136-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4136-263">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f4136-264">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f4136-264">Namespace</span></span><br/>                | <span data-ttu-id="f4136-265">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f4136-265">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f4136-266">MOF</span><span class="sxs-lookup"><span data-stu-id="f4136-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4136-267"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4136-267"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4136-268">DLL</span><span class="sxs-lookup"><span data-stu-id="f4136-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4136-269"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4136-269"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4136-270">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4136-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4136-271">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="f4136-271">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="f4136-272">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="f4136-272">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="f4136-273">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="f4136-273">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="f4136-274">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f4136-274">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

