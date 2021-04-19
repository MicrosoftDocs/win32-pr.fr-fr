---
description: Importe des certificats à partir d’un fichier dans le magasin.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541552"
---
# <a name="storeload-method"></a><span data-ttu-id="c3978-103">Store. Load, méthode</span><span class="sxs-lookup"><span data-stu-id="c3978-103">Store.Load method</span></span>

<span data-ttu-id="c3978-104">\[La méthode de **chargement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c3978-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c3978-105">Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c3978-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c3978-106">La méthode **Load** importe des certificats à partir d’un fichier dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="c3978-106">The **Load** method imports certificates from a file into the store.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3978-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3978-107">Syntax</span></span>


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c3978-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3978-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3978-109">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3978-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3978-110">Chaîne qui contient le chemin d’accès à un fichier. cer,. SST,. SPC,. p7s ou. pfx, ou un fichier signé Authenticode.</span><span class="sxs-lookup"><span data-stu-id="c3978-110">The string that contains the path to a .cer, .sst, .spc, .p7s, or .pfx file, or any Authenticode signed file.</span></span>

</dd> <dt>

<span data-ttu-id="c3978-111">*Mot de passe* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c3978-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3978-112">Chaîne qui contient le mot de passe en texte clair dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="c3978-112">The string that contains the plaintext password to the file.</span></span> <span data-ttu-id="c3978-113">Jusqu’à 32 caractères Unicode, y compris un caractère null de fin, peuvent être utilisés pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="c3978-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="c3978-114">Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="c3978-114">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3978-115">*KeyStorageFlag* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c3978-115">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3978-116">Valeur de l’énumération de l' [**indicateur de \_ \_ stockage \_ de clé CAPICOM**](capicom-key-storage-flag.md) qui définit les indicateurs de stockage de clé.</span><span class="sxs-lookup"><span data-stu-id="c3978-116">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="c3978-117">La valeur par défaut est le \_ \_ stockage par clé CAPICOM \_ par défaut.</span><span class="sxs-lookup"><span data-stu-id="c3978-117">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="c3978-118">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3978-118">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c3978-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3978-119">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="c3978-120">Signification</span><span class="sxs-lookup"><span data-stu-id="c3978-120">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="c3978-121"><dt>**\_ \_ \_ valeur par défaut du stockage de la clé CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="c3978-121"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="c3978-122">Stockage de clé par défaut.</span><span class="sxs-lookup"><span data-stu-id="c3978-122">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="c3978-123"><dt>**\_espace de stockage de clé CAPICOM \_ \_ exportable**</dt></span><span class="sxs-lookup"><span data-stu-id="c3978-123"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="c3978-124">La clé peut être exportée.</span><span class="sxs-lookup"><span data-stu-id="c3978-124">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="c3978-125"><dt>**\_clé CAPICOM \_ \_ protégée par l’utilisateur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3978-125"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="c3978-126">La clé est protégée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3978-126">The key is user protected.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3978-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3978-127">Return value</span></span>

<span data-ttu-id="c3978-128">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c3978-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3978-129">Notes</span><span class="sxs-lookup"><span data-stu-id="c3978-129">Remarks</span></span>

<span data-ttu-id="c3978-130">Si la méthode **Load** est appelée sur un magasin de mémoire, tous les conteneurs de clé créés sont supprimés lors de la suppression du magasin de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c3978-130">If the **Load** method is called on a memory store, any key containers that are created will be deleted when the memory store is deleted.</span></span> <span data-ttu-id="c3978-131">Par exemple, si un fichier. pfx est chargé dans un magasin de mémoire et ajouté ultérieurement à un magasin système (tel que le magasin My) à partir du magasin de mémoire, le certificat du magasin My ne contient pas de clé.</span><span class="sxs-lookup"><span data-stu-id="c3978-131">For example, if a .pfx file is loaded into a memory store and later added to a system store (such as the My store) from the memory store, the certificate in the My store will not contain a key.</span></span> <span data-ttu-id="c3978-132">Dans ce cas, le fichier. pfx doit être chargé directement dans le magasin My.</span><span class="sxs-lookup"><span data-stu-id="c3978-132">In this case, the .pfx file should be loaded directly into the My store.</span></span>

<span data-ttu-id="c3978-133">Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="c3978-133">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="c3978-134">Si le mot de passe ne parvient pas à déchiffrer le fichier de clé privée, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) par défaut doit être interrogé.</span><span class="sxs-lookup"><span data-stu-id="c3978-134">If the password fails to decrypt the private key file, then the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) should be queried.</span></span> <span data-ttu-id="c3978-135">Si le fournisseur de services de chiffrement par défaut est le fournisseur de services de chiffrement de base Microsoft et que l’opération de déchiffrement échoue, l’opération de déchiffrement doit être retentée avec le fournisseur de services de chiffrement fort Microsoft ou le fournisseur de services de chiffrement amélioré</span><span class="sxs-lookup"><span data-stu-id="c3978-135">If the default CSP is the Microsoft Base Cryptographic Provider and the decrypt operation fails, then the decrypt operation should be tried again with the Microsoft Strong Cryptographic Provider or Microsoft Enhanced Cryptographic Provider, whichever is available.</span></span>

<span data-ttu-id="c3978-136">Si le certificat en cours de chargement dans le magasin est le même que celui qui existe déjà, la méthode **Load** supprime le certificat existant du magasin, puis ajoute le nouveau certificat.</span><span class="sxs-lookup"><span data-stu-id="c3978-136">If the certificate being loaded into the store is the same as one that is already there, the **Load** method will delete the existing certificate from the store and then add the new certificate.</span></span> <span data-ttu-id="c3978-137">Le nouveau certificat héritera des propriétés du certificat existant.</span><span class="sxs-lookup"><span data-stu-id="c3978-137">The new certificate will inherit properties from the existing certificate.</span></span> <span data-ttu-id="c3978-138">Le conteneur de clé privée existant est remplacé par le nouveau conteneur de clé privée.</span><span class="sxs-lookup"><span data-stu-id="c3978-138">The existing private key container is replaced by the new private key container.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3978-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3978-139">Requirements</span></span>



| <span data-ttu-id="c3978-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3978-140">Requirement</span></span> | <span data-ttu-id="c3978-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3978-141">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3978-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c3978-142">Redistributable</span></span><br/> | <span data-ttu-id="c3978-143">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3978-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c3978-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c3978-144">DLL</span></span><br/>             | <dl> <span data-ttu-id="c3978-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3978-145"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3978-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3978-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3978-147">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="c3978-147">**Store**</span></span>](store.md)
</dt> </dl>

 

 
