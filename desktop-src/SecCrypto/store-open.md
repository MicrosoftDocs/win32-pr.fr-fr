---
description: Ouvre un magasin de certificats spécifié.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545918"
---
# <a name="storeopen-method"></a><span data-ttu-id="3d6de-103">Store. Open, méthode</span><span class="sxs-lookup"><span data-stu-id="3d6de-103">Store.Open method</span></span>

<span data-ttu-id="3d6de-104">\[La méthode **Open** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3d6de-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3d6de-105">Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3d6de-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3d6de-106">La méthode **Open** ouvre un [*magasin de certificats*](../secgloss/c-gly.md)spécifié.</span><span class="sxs-lookup"><span data-stu-id="3d6de-106">The **Open** method opens a specified [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="3d6de-107">Par défaut, l’emplacement du magasin \_ de l’utilisateur actuel CAPICOM \_ \_ et CAPICOM \_ My \_ Store Store sont ouverts en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d6de-107">By default, the CAPICOM\_CURRENT\_USER\_STORE location and CAPICOM\_MY\_STORE store are opened as read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6de-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d6de-108">Syntax</span></span>


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3d6de-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d6de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6de-110">*StoreLocation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3d6de-110">*StoreLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6de-111">Valeur de l’énumération de l' [ \_ \_ emplacement du magasin CAPICOM](capicom-store-location.md) qui indique l’emplacement du magasin à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="3d6de-111">A value of the [CAPICOM\_STORE\_LOCATION](capicom-store-location.md) enumeration that indicates the location of the store to be opened.</span></span> <span data-ttu-id="3d6de-112">La valeur par défaut est le magasin de l' \_ utilisateur actuel CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3d6de-112">The default value is CAPICOM\_CURRENT\_USER\_STORE.</span></span> <span data-ttu-id="3d6de-113">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d6de-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3d6de-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d6de-114">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="3d6de-115">Signification</span><span class="sxs-lookup"><span data-stu-id="3d6de-115">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <span data-ttu-id="3d6de-116"><dt>**magasin d’utilisateurs de CAPICOM \_ active \_ Directory \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-116"><dt>**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="3d6de-117">Le magasin est un magasin de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3d6de-117">The store is an Active Directory store.</span></span> <span data-ttu-id="3d6de-118">Aucune erreur ne sera générée si un magasin de Active Directory est ouvert en lecture/écriture, mais que les modifications apportées au magasin ne seront pas conservées.</span><span class="sxs-lookup"><span data-stu-id="3d6de-118">No error will be generated if an Active Directory store is opened as read/write, but any changes to the store will not be persisted.</span></span> <span data-ttu-id="3d6de-119">Impossible d’ajouter ou de supprimer des certificats dans des magasins de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3d6de-119">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <span data-ttu-id="3d6de-120"><dt>**magasin de l' \_ utilisateur actuel CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-120"><dt>**CAPICOM\_CURRENT\_USER\_STORE**</dt></span></span> </dl>                             | <span data-ttu-id="3d6de-121">Le magasin est un magasin de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="3d6de-121">The store is a current user store.</span></span> <span data-ttu-id="3d6de-122">Un magasin de l’utilisateur actuel peut être un magasin en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d6de-122">A current user store may be a read/write store.</span></span> <span data-ttu-id="3d6de-123">Si c’est le cas, les modifications apportées au contenu du magasin sont conservées.</span><span class="sxs-lookup"><span data-stu-id="3d6de-123">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <span data-ttu-id="3d6de-124"><dt>**base de l' \_ ordinateur local CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-124"><dt>**CAPICOM\_LOCAL\_MACHINE\_STORE**</dt></span></span> </dl>                          | <span data-ttu-id="3d6de-125">Le magasin est un magasin de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3d6de-125">The store is a local computer store.</span></span> <span data-ttu-id="3d6de-126">Les magasins d’ordinateurs locaux peuvent être des magasins de lecture/écriture uniquement si l’utilisateur dispose d’autorisations de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d6de-126">Local computer stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="3d6de-127">Si l’utilisateur dispose d’autorisations de lecture/écriture et si le magasin est ouvert en lecture/écriture, les modifications apportées au contenu du magasin sont conservées.</span><span class="sxs-lookup"><span data-stu-id="3d6de-127">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <span data-ttu-id="3d6de-128"><dt>**\_magasin mémoire CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-128"><dt>**CAPICOM\_MEMORY\_STORE**</dt></span></span> </dl>                                                | <span data-ttu-id="3d6de-129">Le magasin est un magasin de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3d6de-129">The store is a memory store.</span></span> <span data-ttu-id="3d6de-130">Les modifications apportées au contenu du magasin ne sont pas conservées.</span><span class="sxs-lookup"><span data-stu-id="3d6de-130">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <span data-ttu-id="3d6de-131"><dt>**\_magasin d’utilisateurs de \_ carte à puce \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-131"><dt>**CAPICOM\_SMART\_CARD\_USER\_STORE**</dt></span></span> </dl>                   | <span data-ttu-id="3d6de-132">Le magasin est le groupe de cartes à puce actuelles.</span><span class="sxs-lookup"><span data-stu-id="3d6de-132">The store is the group of present smart cards.</span></span> <span data-ttu-id="3d6de-133">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="3d6de-133">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="3d6de-134">*StoreName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3d6de-134">*StoreName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6de-135">Chaîne qui contient le nom du magasin de certificats système à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="3d6de-135">A string that contains the name of the system certificate store to be opened.</span></span> <span data-ttu-id="3d6de-136">La valeur par défaut est CAPICOM \_ My \_ Store.</span><span class="sxs-lookup"><span data-stu-id="3d6de-136">The default value is CAPICOM\_MY\_STORE.</span></span> <span data-ttu-id="3d6de-137">Si le magasin est ouvert à partir d’un script Web, le caractère de barre oblique inverse ( \\ ) n’est pas autorisé dans le nom.</span><span class="sxs-lookup"><span data-stu-id="3d6de-137">If the store is opened from a web script, the backslash (\\) character is not allowed in the name.</span></span> <span data-ttu-id="3d6de-138">En plus des magasins définis par le système, les magasins définis par l’utilisateur peuvent être ouverts.</span><span class="sxs-lookup"><span data-stu-id="3d6de-138">In addition to stores defined by the system, user-defined stores can be opened.</span></span>

<span data-ttu-id="3d6de-139">Ce paramètre peut être un magasin défini par l’utilisateur ou l’un des magasins de certificats système suivants.</span><span class="sxs-lookup"><span data-stu-id="3d6de-139">This parameter can be a user-defined store or one of the following system certificate stores.</span></span>



| <span data-ttu-id="3d6de-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d6de-140">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="3d6de-141">Signification</span><span class="sxs-lookup"><span data-stu-id="3d6de-141">Meaning</span></span>                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <span data-ttu-id="3d6de-142"><dt>**\_magasin d’autorités de certification CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-142"><dt>**CAPICOM\_CA\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="3d6de-143">Magasin d’autorités de certification.</span><span class="sxs-lookup"><span data-stu-id="3d6de-143">CA store.</span></span> <span data-ttu-id="3d6de-144">Ce magasin est utilisé pour stocker les certificats intermédiaires de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="3d6de-144">This store is used to store intermediate CA certificates.</span></span><br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <span data-ttu-id="3d6de-145"><dt>**CAPICOM \_ My \_ Store**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-145"><dt>**CAPICOM\_MY\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="3d6de-146">Mon magasin.</span><span class="sxs-lookup"><span data-stu-id="3d6de-146">My store.</span></span> <span data-ttu-id="3d6de-147">Ce magasin est utilisé pour les certificats personnels d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d6de-147">This store is used for a user's personal certificates.</span></span><br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <span data-ttu-id="3d6de-148"><dt>**\_autre \_ magasin**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-148"><dt>**CAPICOM\_OTHER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="3d6de-149">Magasin AddressBook.</span><span class="sxs-lookup"><span data-stu-id="3d6de-149">AddressBook store.</span></span> <span data-ttu-id="3d6de-150">Ce magasin est utilisé pour conserver les certificats des autres.</span><span class="sxs-lookup"><span data-stu-id="3d6de-150">This store is used to keep the certificates of others.</span></span><br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <span data-ttu-id="3d6de-151"><dt>**\_magasin racine CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-151"><dt>**CAPICOM\_ROOT\_STORE**</dt></span></span> </dl>    | <span data-ttu-id="3d6de-152">Magasin racine.</span><span class="sxs-lookup"><span data-stu-id="3d6de-152">Root store.</span></span> <span data-ttu-id="3d6de-153">Ce magasin est utilisé pour stocker l’autorité de certification racine et les certificats de confiance auto-signés.</span><span class="sxs-lookup"><span data-stu-id="3d6de-153">This store is used to store the root CA and self-signed, trusted certificates.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3d6de-154">*OpenMode* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3d6de-154">*OpenMode* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6de-155">Valeur de l’énumération du mode d’ouverture de l' [ \_ entrepôt d’enregistrement \_ \_ CAPICOM](capicom-store-open-mode.md) qui indique le mode d’ouverture du magasin.</span><span class="sxs-lookup"><span data-stu-id="3d6de-155">A value of the [CAPICOM\_STORE\_OPEN\_MODE](capicom-store-open-mode.md) enumeration that indicates the open mode of the store.</span></span> <span data-ttu-id="3d6de-156">La valeur par défaut est CAPICOM \_ Store \_ ouvert \_ en lecture \_ seule.</span><span class="sxs-lookup"><span data-stu-id="3d6de-156">The default value is CAPICOM\_STORE\_OPEN\_READ\_ONLY.</span></span> <span data-ttu-id="3d6de-157">Si le magasin est ouvert à partir d’un script Web, cette valeur est forcée à l’ouverture de la base de l' \_ emplacement de stockage \_ \_ \_ uniquement.</span><span class="sxs-lookup"><span data-stu-id="3d6de-157">If the store is opened from a web script, this value is forced to CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY.</span></span> <span data-ttu-id="3d6de-158">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d6de-158">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3d6de-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d6de-159">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="3d6de-160">Signification</span><span class="sxs-lookup"><span data-stu-id="3d6de-160">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <span data-ttu-id="3d6de-161"><dt>**\_ \_ \_ maximum \_ autorisé pour le magasin CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-161"><dt>**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</dt></span></span> </dl> | <span data-ttu-id="3d6de-162">Ouvre le magasin en mode lecture/écriture si l’utilisateur dispose d’autorisations de lecture/écriture. Sinon, ouvrez le magasin en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d6de-162">Open the store in read/write mode if the user has read/write permissions; otherwise, open the store in read-only mode.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <span data-ttu-id="3d6de-163"><dt>**le magasin CAPICOM \_ est \_ ouvert \_ en lecture \_ seule**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-163"><dt>**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</dt></span></span> </dl>                   | <span data-ttu-id="3d6de-164">Ouvrez le magasin en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d6de-164">Open the store in read-only mode.</span></span><br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <span data-ttu-id="3d6de-165"><dt>**ouverture de la \_ \_ \_ lecture écriture du \_ magasin CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-165"><dt>**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</dt></span></span> </dl>                | <span data-ttu-id="3d6de-166">Ouvrez le magasin en mode lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d6de-166">Open the store in read/write mode.</span></span><br/>                                                                                     |



 

<span data-ttu-id="3d6de-167">Les indicateurs suivants peuvent être combinés avec les valeurs du tableau précédent à l’aide d’une opération **or** logique.</span><span class="sxs-lookup"><span data-stu-id="3d6de-167">The following flags can be combined with the values in the previous table by using a logical-**OR** operation.</span></span>



| <span data-ttu-id="3d6de-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d6de-168">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="3d6de-169">Signification</span><span class="sxs-lookup"><span data-stu-id="3d6de-169">Meaning</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <span data-ttu-id="3d6de-170"><dt>**le magasin CAPICOM \_ est \_ ouvert \_ \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-170"><dt>**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</dt></span></span> </dl>          | <span data-ttu-id="3d6de-171">Ouvrir les magasins existants uniquement ; ne créez pas de nouveau magasin.</span><span class="sxs-lookup"><span data-stu-id="3d6de-171">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="3d6de-172">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="3d6de-172">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <span data-ttu-id="3d6de-173"><dt>**l’ouverture du \_ magasin \_ CAPICOM \_ inclut \_ Archived**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-173"><dt>**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</dt></span></span> </dl> | <span data-ttu-id="3d6de-174">Incluez les certificats archivés lors de l’utilisation du magasin.</span><span class="sxs-lookup"><span data-stu-id="3d6de-174">Include archived certificates when using the store.</span></span> <span data-ttu-id="3d6de-175">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="3d6de-175">Introduced in CAPICOM 2.0.</span></span><br/>   |



 

<span data-ttu-id="3d6de-176">Les magasins situés dans certains emplacements ne peuvent être ouverts qu’en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d6de-176">Stores in some locations can be opened only in read-only mode.</span></span> <span data-ttu-id="3d6de-177">Cela inclut tous les magasins dans CAPICOM \_ local \_ machine \_ Store pour lesquels l’utilisateur ne dispose pas d’autorisations en écriture.</span><span class="sxs-lookup"><span data-stu-id="3d6de-177">These include all stores in CAPICOM\_LOCAL\_MACHINE\_STORE for which the user does not have write permissions.</span></span> <span data-ttu-id="3d6de-178">Toute tentative d’ouverture d’un magasin en tant que magasin de lecture/écriture sans accès et autorisations appropriés entraîne l’échec de la méthode **Open** .</span><span class="sxs-lookup"><span data-stu-id="3d6de-178">Attempts to open a store as a read/write store without proper access and permissions will result in the failure of the **Open** method.</span></span> <span data-ttu-id="3d6de-179">Les magasins de Active Directory peuvent être ouverts en tant que magasin de lecture/écriture sans échec de la méthode **Open** , mais les modifications apportées au magasin ne sont pas rendues persistantes.</span><span class="sxs-lookup"><span data-stu-id="3d6de-179">Active Directory stores can be opened as a read/write store without failure of the **Open** method, but changes to the store will not be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6de-180">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d6de-180">Return value</span></span>

<span data-ttu-id="3d6de-181">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3d6de-181">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d6de-182">Notes</span><span class="sxs-lookup"><span data-stu-id="3d6de-182">Remarks</span></span>

<span data-ttu-id="3d6de-183">Si cette méthode est appelée sur un magasin de cartes à puce, d’autres interfaces utilisateur de carte à puce peuvent être appelées.</span><span class="sxs-lookup"><span data-stu-id="3d6de-183">If this method is called on a SmartCard store, additional SmartCard user interfaces may be invoked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d6de-184">Lorsque cette méthode est appelée à partir d’un script Web, le script doit accéder aux certificats numériques sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3d6de-184">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="3d6de-185">Si vous autorisez le script à accéder à vos certificats numériques, le site Web à partir duquel le script est exécuté aura également accès aux informations personnelles stockées dans les certificats.</span><span class="sxs-lookup"><span data-stu-id="3d6de-185">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="3d6de-186">La première fois que cette méthode est appelée à partir d’un domaine particulier, une boîte de dialogue est générée dans laquelle l’utilisateur doit indiquer si l’accès aux certificats doit être autorisé.</span><span class="sxs-lookup"><span data-stu-id="3d6de-186">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span> <span data-ttu-id="3d6de-187">Les magasins ouverts à partir d’un script Web forcent automatiquement l’indicateur de l’ouverture de l’ouverture de l' \_ emplacement existant du magasin CAPICOM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3d6de-187">Stores opened from a web script automatically force the CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY flag.</span></span>

 

<span data-ttu-id="3d6de-188">Si *StoreLocation* est un **magasin d' \_ \_ utilisateurs de \_ carte \_ à puce** CAPICOM, *StoreName* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="3d6de-188">If *StoreLocation* is **CAPICOM\_SMART\_CARD\_USER\_STORE**, *StoreName* is ignored.</span></span> <span data-ttu-id="3d6de-189">Dans ce cas, CAPICOM lit tous les certificats de tous les lecteurs disponibles qui contiennent une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="3d6de-189">In this case, CAPICOM reads all certificates from all available readers that contain a smart card.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6de-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d6de-190">Requirements</span></span>



| <span data-ttu-id="3d6de-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d6de-191">Requirement</span></span> | <span data-ttu-id="3d6de-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d6de-192">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6de-193">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3d6de-193">Redistributable</span></span><br/> | <span data-ttu-id="3d6de-194">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="3d6de-194">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3d6de-195">DLL</span><span class="sxs-lookup"><span data-stu-id="3d6de-195">DLL</span></span><br/>             | <dl> <span data-ttu-id="3d6de-196"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d6de-196"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d6de-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d6de-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6de-198">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="3d6de-198">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="3d6de-199">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="3d6de-199">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="3d6de-200">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="3d6de-200">**Close**</span></span>](store-close.md)
</dt> </dl>

 

 
