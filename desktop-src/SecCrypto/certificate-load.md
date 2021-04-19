---
description: Importe un certificat à partir d’un fichier.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'ICertificate2 :: Load, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537321"
---
# <a name="icertificate2load-method"></a><span data-ttu-id="53f1e-103">ICertificate2 :: Load, méthode</span><span class="sxs-lookup"><span data-stu-id="53f1e-103">ICertificate2::Load method</span></span>

<span data-ttu-id="53f1e-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="53f1e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="53f1e-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="53f1e-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="53f1e-106">La méthode **Load** importe un certificat à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="53f1e-106">The **Load** method imports a certificate from a file.</span></span> <span data-ttu-id="53f1e-107">Cette méthode a été introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="53f1e-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f1e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53f1e-108">Syntax</span></span>


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a><span data-ttu-id="53f1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53f1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f1e-110">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53f1e-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f1e-111">Chaîne qui contient le chemin d’accès à un fichier. cer ou. pfx qui contient les données de certificat.</span><span class="sxs-lookup"><span data-stu-id="53f1e-111">A string that contains the path to a .cer or .pfx file that contains the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="53f1e-112">*Mot de passe* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="53f1e-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53f1e-113">Chaîne qui contient le mot de passe en [*texte clair*](../secgloss/p-gly.md) dans le fichier de [*clé privée*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="53f1e-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password to the [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="53f1e-114">Le mot de passe peut contenir jusqu’à 32 caractères Unicode, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="53f1e-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="53f1e-115">Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="53f1e-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="53f1e-116">*KeyStorageFlag* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="53f1e-116">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53f1e-117">Valeur de l’énumération de l' [**indicateur de \_ \_ stockage \_ de clé CAPICOM**](capicom-key-storage-flag.md) qui définit les indicateurs de stockage de clé.</span><span class="sxs-lookup"><span data-stu-id="53f1e-117">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="53f1e-118">La valeur par défaut est le \_ \_ stockage par clé CAPICOM \_ par défaut.</span><span class="sxs-lookup"><span data-stu-id="53f1e-118">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="53f1e-119">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="53f1e-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="53f1e-120">Value</span><span class="sxs-lookup"><span data-stu-id="53f1e-120">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="53f1e-121">Signification</span><span class="sxs-lookup"><span data-stu-id="53f1e-121">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="53f1e-122"><dt>**\_ \_ \_ valeur par défaut du stockage de la clé CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1e-122"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="53f1e-123">Stockage de clé par défaut.</span><span class="sxs-lookup"><span data-stu-id="53f1e-123">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="53f1e-124"><dt>**\_espace de stockage de clé CAPICOM \_ \_ exportable**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1e-124"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="53f1e-125">La clé peut être exportée.</span><span class="sxs-lookup"><span data-stu-id="53f1e-125">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="53f1e-126"><dt>**\_clé CAPICOM \_ \_ protégée par l’utilisateur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1e-126"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="53f1e-127">La clé est protégée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53f1e-127">The key is user protected.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53f1e-128">*Emplacement des Keyposition* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="53f1e-128">*KeyLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53f1e-129">Valeur de l’énumération de l' [**\_ \_ emplacement de la clé CAPICOM**](capicom-key-location.md) qui définit les types d’emplacement de clé.</span><span class="sxs-lookup"><span data-stu-id="53f1e-129">A value of the [**CAPICOM\_KEY\_LOCATION**](capicom-key-location.md) enumeration that defines key location types.</span></span> <span data-ttu-id="53f1e-130">La valeur par défaut est la \_ \_ clé utilisateur actuelle CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="53f1e-130">The default value is CAPICOM\_CURRENT\_USER\_KEY.</span></span> <span data-ttu-id="53f1e-131">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="53f1e-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="53f1e-132">Value</span><span class="sxs-lookup"><span data-stu-id="53f1e-132">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="53f1e-133">Signification</span><span class="sxs-lookup"><span data-stu-id="53f1e-133">Meaning</span></span>                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <span data-ttu-id="53f1e-134"><dt>**clé de l' \_ utilisateur actuel CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1e-134"><dt>**CAPICOM\_CURRENT\_USER\_KEY**</dt></span></span> </dl>    | <span data-ttu-id="53f1e-135">La clé est une clé utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53f1e-135">The key is a user key.</span></span><br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <span data-ttu-id="53f1e-136"><dt>**\_clé d’ordinateur local \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1e-136"><dt>**CAPICOM\_LOCAL\_MACHINE\_KEY**</dt></span></span> </dl> | <span data-ttu-id="53f1e-137">La clé est une clé d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="53f1e-137">The key is a machine key.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f1e-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53f1e-138">Return value</span></span>

<span data-ttu-id="53f1e-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="53f1e-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f1e-140">Notes</span><span class="sxs-lookup"><span data-stu-id="53f1e-140">Remarks</span></span>

<span data-ttu-id="53f1e-141">Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="53f1e-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f1e-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53f1e-142">Requirements</span></span>



| <span data-ttu-id="53f1e-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53f1e-143">Requirement</span></span> | <span data-ttu-id="53f1e-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="53f1e-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53f1e-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="53f1e-145">End of client support</span></span><br/> | <span data-ttu-id="53f1e-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53f1e-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="53f1e-147">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="53f1e-147">End of server support</span></span><br/> | <span data-ttu-id="53f1e-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53f1e-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="53f1e-149">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="53f1e-149">Redistributable</span></span><br/>       | <span data-ttu-id="53f1e-150">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="53f1e-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="53f1e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="53f1e-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="53f1e-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f1e-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
