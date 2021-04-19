---
title: Classe MDM_WindowsLicensing
description: La \_ classe MDM WindowsLicensing est conçue pour les scénarios de gestion des licences.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- Classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, Description
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509520"
---
# <a name="mdm_windowslicensing-class"></a><span data-ttu-id="19920-105">\_Classe WINDOWSLICENSING MDM</span><span class="sxs-lookup"><span data-stu-id="19920-105">MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="19920-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="19920-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19920-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="19920-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19920-108">La classe **MDM \_ WindowsLicensing** est conçue pour les scénarios de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="19920-108">The **MDM\_WindowsLicensing** class is designed for licensing related management scenarios.</span></span> <span data-ttu-id="19920-109">Actuellement, l’étendue est limitée aux mises à niveau d’édition des appareils Windows 10 Desktop et mobile, tels que Windows 10 professionnel vers Windows 10 entreprise.</span><span class="sxs-lookup"><span data-stu-id="19920-109">Currently the scope is limited to edition upgrades of Windows 10 desktop and mobile devices, such as Windows 10 Pro to Windows 10 Enterprise.</span></span> <span data-ttu-id="19920-110">En outre, ce CSP offre la possibilité d’activer ou de modifier la clé de produit des appareils Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="19920-110">In addition, this CSP provides the capability to activate or change the product key of Windows 10 desktop devices.</span></span>

<span data-ttu-id="19920-111">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="19920-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19920-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19920-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a><span data-ttu-id="19920-113">Membres</span><span class="sxs-lookup"><span data-stu-id="19920-113">Members</span></span>

<span data-ttu-id="19920-114">La **classe \_ WindowsLicensing MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="19920-114">The **MDM\_WindowsLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="19920-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19920-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="19920-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19920-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="19920-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19920-117">Methods</span></span>

<span data-ttu-id="19920-118">La classe **MDM \_ WindowsLicensing** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="19920-118">The **MDM\_WindowsLicensing** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="19920-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="19920-119">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="19920-120">Description</span><span class="sxs-lookup"><span data-stu-id="19920-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="19920-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="19920-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="19920-122">Installe une clé de produit pour les appareils Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="19920-122">Installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="19920-123">Ne redémarre pas.</span><span class="sxs-lookup"><span data-stu-id="19920-123">Does not reboot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="19920-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="19920-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="19920-125">Méthode permettant de vérifier si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit Windows 10 pour les appareils de bureau.</span><span class="sxs-lookup"><span data-stu-id="19920-125">Method to check if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="19920-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="19920-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="19920-127">Fournissez une licence pour une mise à niveau d’édition des appareils Windows 10 mobile.</span><span class="sxs-lookup"><span data-stu-id="19920-127">Provide a license for an edition upgrade of Windows 10 mobile devices.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="19920-128">Ce processus de mise à niveau ne nécessite pas de redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="19920-128">This upgrade process does not require a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="19920-129">Le type de date est XML.</span><span class="sxs-lookup"><span data-stu-id="19920-129">The date type is XML.</span></span><br/> <span data-ttu-id="19920-130">L’opération prise en charge est Execute.</span><span class="sxs-lookup"><span data-stu-id="19920-130">The supported operation is Execute.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="19920-131">Le contenu du fichier de licence XML doit être correctement placé dans une séquence d’échappement (c’est-à-dire qu’il ne doit pas simplement être un fichier XML copié), sinon la mise à niveau de l’édition sur les appareils Windows 10 Mobile échoue.</span><span class="sxs-lookup"><span data-stu-id="19920-131">The XML license file contents must be properly escaped (that is, it should not simply be a copied XML), otherwise the edition upgrade on Windows 10 mobile devices will fail.</span></span> <span data-ttu-id="19920-132">Pour plus d’informations sur la séquence d’échappement correcte du fichier de licence XML, consultez la section 2,4 de la <a href="https://www.w3.org/TR/xml/">spécification XML du W3C</a>. Le fichier de licence XML est acquis auprès du centre de gestion des licences en volume Microsoft.</span><span class="sxs-lookup"><span data-stu-id="19920-132">For more information on proper escaping of the XML license file, see Section 2.4 of the <a href="https://www.w3.org/TR/xml/">W3C XML spec</a>. The XML license file is acquired from the Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="19920-133">Votre organisation doit avoir un contrat de licence en volume avec Microsoft pour accéder au portail.</span><span class="sxs-lookup"><span data-stu-id="19920-133">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="19920-134">Voici les chemins de mise à niveau d’édition valides lors de l’utilisation de ce nœud via un package MDM ou approvisionnement :</span><span class="sxs-lookup"><span data-stu-id="19920-134">The following are valid edition upgrade paths when using this node through an MDM or provisioning package:</span></span>
<ul>
<li><span data-ttu-id="19920-135">Windows 10 Mobileto Windows 10 Mobile entreprise</span><span class="sxs-lookup"><span data-stu-id="19920-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span></span><br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="19920-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="19920-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="19920-137">Déclenche l’appareil pour prendre la clé de produit et mettre à niveau l’édition du client.</span><span class="sxs-lookup"><span data-stu-id="19920-137">Triggers the device to take the product key and upgrade the edition of the client.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19920-138">Ce processus de mise à niveau nécessite un redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="19920-138">This upgrade process requires a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="19920-139">L’opération prise en charge est Execute.</span><span class="sxs-lookup"><span data-stu-id="19920-139">The supported operation is Execute.</span></span><br/> <span data-ttu-id="19920-140">Lorsqu’une clé de produit est envoyée d’un serveur MDM à l’appareil d’un utilisateur, <strong>changepk.exe</strong> s’exécute à l’aide de la clé de produit.</span><span class="sxs-lookup"><span data-stu-id="19920-140">When a product key is pushed from an MDM server to a user's device, <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="19920-141">Une fois l’opération terminée, une notification s’affiche pour l’utilisateur qu’une nouvelle édition de Windows 10 est disponible.</span><span class="sxs-lookup"><span data-stu-id="19920-141">After it completes, a notification is shown to the user that a new edition of Windows 10 is available.</span></span> <span data-ttu-id="19920-142">L’utilisateur peut ensuite redémarrer son système manuellement ou, au bout de deux heures, l’appareil redémarrera automatiquement pour terminer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="19920-142">The user can then restart their system manually or, after two hours, the device will restart automatically to complete the upgrade.</span></span> <span data-ttu-id="19920-143">L’utilisateur recevra une notification de rappel 10 minutes avant le redémarrage automatique.</span><span class="sxs-lookup"><span data-stu-id="19920-143">The user will receive a reminder notification 10 minutes before the automatic restart.</span></span><br/> <span data-ttu-id="19920-144">Après le redémarrage de l’appareil, le processus de mise à niveau d’édition se termine.</span><span class="sxs-lookup"><span data-stu-id="19920-144">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="19920-145">L’utilisateur recevra une notification indiquant la réussite de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="19920-145">The user will receive a notification of the successful upgrade.</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="19920-146">Si une autre stratégie requiert un redémarrage du système qui se produit lorsque <strong>changepk.exe</strong> est en cours d’exécution, la mise à niveau de l’édition échouera.</span><span class="sxs-lookup"><span data-stu-id="19920-146">If another policy requires a system reboot that occurs when <strong>changepk.exe</strong> is running, the edition upgrade will fail.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="19920-147">Si une clé de produit est entrée dans un package de configuration et que l’utilisateur commence l’installation du package, une notification s’affiche pour l’utilisateur que son système redémarrera pour terminer l’installation du package.</span><span class="sxs-lookup"><span data-stu-id="19920-147">If a product key is entered in a provisioning package and the user begins installation of the package, a notification is shown to the user that their system will restart to complete the package installation.</span></span> <span data-ttu-id="19920-148">En cas de consentement explicite de l’utilisateur pour continuer, le package continue l’installation et <strong>changepk.exe</strong> exécute à l’aide de la clé de produit.</span><span class="sxs-lookup"><span data-stu-id="19920-148">Upon explicit consent from the user to proceed, the package continues installation and <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="19920-149">L’utilisateur recevra une notification de rappel 30 secondes avant le redémarrage automatique.</span><span class="sxs-lookup"><span data-stu-id="19920-149">The user will receive a reminder notification 30 seconds before the automatic restart.</span></span> <br/> <span data-ttu-id="19920-150">Après le redémarrage de l’appareil, le processus de mise à niveau d’édition se termine.</span><span class="sxs-lookup"><span data-stu-id="19920-150">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="19920-151">L’utilisateur recevra une notification indiquant la réussite de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="19920-151">The user will receive a notification of the successful upgrade.</span></span> <br/> <span data-ttu-id="19920-152">Ce nœud peut également être utilisé pour activer ou modifier une clé de produit sur une édition particulière du périphérique Windows 10 Desktop en entrant une clé de produit.</span><span class="sxs-lookup"><span data-stu-id="19920-152">This node can also be used to activate or change a product key on a particular edition of Windows 10 desktop device by entering a product key.</span></span> <span data-ttu-id="19920-153">L’activation ou la modification d’une clé de produit ne nécessite pas de redémarrage et est un processus silencieux pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19920-153">Activation or changing a product key does not require a reboot and is a silent process for the user.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="19920-154">La clé de produit entrée doit comporter 29 caractères (en d’autres lettres), sinon la modification de l’activation, de la mise à niveau de l’édition ou de la clé de produit sur les appareils Windows 10 Desktop échouera.</span><span class="sxs-lookup"><span data-stu-id="19920-154">The product key entered must be 29 characters (that is, it should include dashes), otherwise the activation, edition upgrade, or product key change on Windows 10 desktop devices will fail.</span></span> <span data-ttu-id="19920-155">La clé de produit est acquise auprès du centre de gestion des licences en volume Microsoft.</span><span class="sxs-lookup"><span data-stu-id="19920-155">The product key is acquired from Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="19920-156">Votre organisation doit avoir un contrat de licence en volume avec Microsoft pour accéder au portail.</span><span class="sxs-lookup"><span data-stu-id="19920-156">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="19920-157">Voici les chemins de mise à niveau d’édition valides lors de l’utilisation de ce nœud via un MDM :</span><span class="sxs-lookup"><span data-stu-id="19920-157">The following are valid edition upgrade paths when using this node through an MDM:</span></span>
<ul>
<li><span data-ttu-id="19920-158">Windows 10 entreprise vers Windows 10 éducation</span><span class="sxs-lookup"><span data-stu-id="19920-158">Windows 10 Enterprise to Windows 10 Education</span></span></li>
<li><span data-ttu-id="19920-159">Windows 10 famille à Windows 10 éducation</span><span class="sxs-lookup"><span data-stu-id="19920-159">Windows 10 Home to Windows 10 Education</span></span></li>
<li><span data-ttu-id="19920-160">Windows 10 professionnel vers Windows 10 éducation</span><span class="sxs-lookup"><span data-stu-id="19920-160">Windows 10 Pro to Windows 10 Education</span></span></li>
<li><span data-ttu-id="19920-161">Windows 10 professionnel vers Windows 10 entreprise</span><span class="sxs-lookup"><span data-stu-id="19920-161">Windows 10 Pro to Windows 10 Enterprise</span></span></li>
</ul>
<br/> <span data-ttu-id="19920-162">L’activation ou la modification d’une clé de produit peut être effectuée sur les éditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="19920-162">Activation or changing a product key can be carried out on the following editions:</span></span>
<ul>
<li><span data-ttu-id="19920-163">Windows 10 Éducation</span><span class="sxs-lookup"><span data-stu-id="19920-163">Windows 10 Education</span></span></li>
<li><span data-ttu-id="19920-164">Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="19920-164">Windows 10 Enterprise</span></span></li>
<li><span data-ttu-id="19920-165">Windows 10 Famille</span><span class="sxs-lookup"><span data-stu-id="19920-165">Windows 10 Home</span></span></li>
<li><span data-ttu-id="19920-166">Windows 10 Pro</span><span class="sxs-lookup"><span data-stu-id="19920-166">Windows 10 Pro</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="19920-167">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19920-167">Properties</span></span>

<span data-ttu-id="19920-168">La **classe \_ WindowsLicensing MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="19920-168">The **MDM\_WindowsLicensing** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19920-169">Édition</span><span class="sxs-lookup"><span data-stu-id="19920-169">Edition</span></span>](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19920-170">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="19920-170">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19920-171">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="19920-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19920-172">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19920-172">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19920-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19920-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19920-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19920-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19920-175">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19920-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19920-176">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="19920-176">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="19920-177">LicenseKeyType</span><span class="sxs-lookup"><span data-stu-id="19920-177">LicenseKeyType</span></span>](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19920-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19920-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19920-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="19920-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19920-180">**ID**</span><span class="sxs-lookup"><span data-stu-id="19920-180">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19920-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19920-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19920-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19920-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19920-183">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19920-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19920-184">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="19920-184">Describes the full path to the parent node.</span></span> <span data-ttu-id="19920-185">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="19920-185">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="19920-186">État</span><span class="sxs-lookup"><span data-stu-id="19920-186">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19920-187">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="19920-187">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19920-188">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="19920-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19920-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19920-189">Requirements</span></span>



| <span data-ttu-id="19920-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19920-190">Requirement</span></span> | <span data-ttu-id="19920-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="19920-191">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19920-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19920-192">Minimum supported client</span></span><br/> | <span data-ttu-id="19920-193">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19920-193">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19920-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19920-194">Minimum supported server</span></span><br/> | <span data-ttu-id="19920-195">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="19920-195">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="19920-196">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="19920-196">Namespace</span></span><br/>                | <span data-ttu-id="19920-197">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="19920-197">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="19920-198">MOF</span><span class="sxs-lookup"><span data-stu-id="19920-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19920-199"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19920-199"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="19920-200">DLL</span><span class="sxs-lookup"><span data-stu-id="19920-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19920-201"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19920-201"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19920-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19920-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19920-203">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="19920-203">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

