---
description: Charge un certificat de signature à partir d’un fichier. pfx spécifié.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Signr. Load, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541401"
---
# <a name="signerload-method"></a><span data-ttu-id="5d22f-103">Signr. Load, méthode</span><span class="sxs-lookup"><span data-stu-id="5d22f-103">Signer.Load method</span></span>

<span data-ttu-id="5d22f-104">\[La méthode de **chargement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5d22f-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d22f-105">Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5d22f-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5d22f-106">La méthode **Load** charge un certificat de signature à partir d’un fichier. pfx spécifié.</span><span class="sxs-lookup"><span data-stu-id="5d22f-106">The **Load** method loads a signing certificate from a specified .pfx file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d22f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d22f-107">Syntax</span></span>


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5d22f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d22f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d22f-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5d22f-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5d22f-110">Nom du fichier. pfx qui contient le certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="5d22f-110">Name of the .pfx file that contains the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="5d22f-111">*Mot de passe* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5d22f-111">*Password* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d22f-112">Chaîne contenant le mot de passe en texte clair utilisé pour ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="5d22f-112">String containing the plaintext password used to open the file.</span></span> <span data-ttu-id="5d22f-113">Jusqu’à 32 caractères Unicode, y compris un caractère null de fin, peuvent être utilisés pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5d22f-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="5d22f-114">La valeur par défaut est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="5d22f-114">The default value is an empty string ("").</span></span> <span data-ttu-id="5d22f-115">Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="5d22f-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d22f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d22f-116">Return value</span></span>

<span data-ttu-id="5d22f-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5d22f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d22f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5d22f-118">Remarks</span></span>

<span data-ttu-id="5d22f-119">Cette méthode charge le premier certificat dans le fichier. pfx avec une clé privée qui lui est associée.</span><span class="sxs-lookup"><span data-stu-id="5d22f-119">This method loads the first certificate in the .pfx file that has a private key associated with it.</span></span>

<span data-ttu-id="5d22f-120">Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="5d22f-120">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d22f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d22f-121">Requirements</span></span>



| <span data-ttu-id="5d22f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d22f-122">Requirement</span></span> | <span data-ttu-id="5d22f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d22f-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d22f-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5d22f-124">Redistributable</span></span><br/> | <span data-ttu-id="5d22f-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d22f-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5d22f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5d22f-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="5d22f-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d22f-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d22f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d22f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d22f-129">**Signataire**</span><span class="sxs-lookup"><span data-stu-id="5d22f-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
