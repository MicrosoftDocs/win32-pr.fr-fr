---
description: Supprime le conteneur de clé privée référencé par l’objet PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey. Delete, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542239"
---
# <a name="privatekeydelete-method"></a><span data-ttu-id="6601b-103">PrivateKey. Delete, méthode</span><span class="sxs-lookup"><span data-stu-id="6601b-103">PrivateKey.Delete method</span></span>

<span data-ttu-id="6601b-104">\[La méthode de **suppression** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6601b-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6601b-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6601b-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6601b-106">La méthode **Delete** supprime le conteneur de clé privée référencé par l’objet [**PrivateKey**](privatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="6601b-106">The **Delete** method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6601b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6601b-107">Syntax</span></span>


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a><span data-ttu-id="6601b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6601b-108">Parameters</span></span>

<span data-ttu-id="6601b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6601b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6601b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6601b-110">Return value</span></span>

<span data-ttu-id="6601b-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6601b-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6601b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6601b-112">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6601b-113">Cette méthode supprime le conteneur de clé privée référencé par l’objet [**PrivateKey**](privatekey.md) , ainsi que toutes les clés privées dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="6601b-113">This method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object as well as all private keys in the container.</span></span> <span data-ttu-id="6601b-114">Tout ce qui est chiffré à l’aide des clés publiques correspondant aux clés privées supprimées ne pourra plus être déchiffré.</span><span class="sxs-lookup"><span data-stu-id="6601b-114">Anything encrypted using the public keys corresponding to the deleted private keys will no longer be able to be decrypted.</span></span>

 

<span data-ttu-id="6601b-115">Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="6601b-115">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="6601b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6601b-116">Requirements</span></span>



| <span data-ttu-id="6601b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6601b-117">Requirement</span></span> | <span data-ttu-id="6601b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6601b-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6601b-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6601b-119">Redistributable</span></span><br/> | <span data-ttu-id="6601b-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6601b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6601b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6601b-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="6601b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6601b-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
