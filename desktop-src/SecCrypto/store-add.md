---
description: Ajoute un objet certificat à un magasin de certificats ouvert.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531003"
---
# <a name="storeadd-method"></a><span data-ttu-id="37b91-103">Store. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="37b91-103">Store.Add method</span></span>

<span data-ttu-id="37b91-104">\[La méthode **Add** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="37b91-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="37b91-105">Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="37b91-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="37b91-106">La méthode **Add** ajoute un objet [**certificat**](certificate.md) à un [*magasin de certificats*](../secgloss/c-gly.md)ouvert.</span><span class="sxs-lookup"><span data-stu-id="37b91-106">The **Add** method adds a [**Certificate**](certificate.md) object to an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="37b91-107">Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="37b91-107">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b91-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37b91-108">Syntax</span></span>


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="37b91-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37b91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b91-110">*Certificat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37b91-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b91-111">Expression qui correspond à un objet de [**certificat**](certificate.md) à ajouter au magasin.</span><span class="sxs-lookup"><span data-stu-id="37b91-111">Expression that resolves to a [**Certificate**](certificate.md) object to be added to the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b91-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37b91-112">Return value</span></span>

<span data-ttu-id="37b91-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="37b91-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37b91-114">Notes</span><span class="sxs-lookup"><span data-stu-id="37b91-114">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37b91-115">Lorsque cette méthode est appelée sur un magasin système à partir d’un script Web, le script doit accéder aux certificats numériques sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="37b91-115">When this method is called on a system store from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="37b91-116">Si vous autorisez le script à accéder à vos certificats numériques, le site Web à partir duquel le script est exécuté aura également accès aux informations personnelles stockées dans les certificats.</span><span class="sxs-lookup"><span data-stu-id="37b91-116">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="37b91-117">La première fois que cette méthode est appelée à partir d’un domaine particulier, une boîte de dialogue est générée dans laquelle l’utilisateur doit indiquer si l’accès aux certificats doit être autorisé.</span><span class="sxs-lookup"><span data-stu-id="37b91-117">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="37b91-118">Si le magasin n’est pas ouvert en mode lecture/écriture, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="37b91-118">If the store is not open in read/write mode, this method fails.</span></span> <span data-ttu-id="37b91-119">Bien que cette méthode puisse être utilisée avec les magasins de mémoire, toute modification apportée à un magasin de mémoire n’est pas conservée lors de la fermeture de la Banque.</span><span class="sxs-lookup"><span data-stu-id="37b91-119">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

<span data-ttu-id="37b91-120">Si le certificat ajouté au magasin est le même que celui qui existe déjà, la méthode **Add** supprime le certificat existant du magasin, puis ajoute le nouveau certificat.</span><span class="sxs-lookup"><span data-stu-id="37b91-120">If the certificate being added to the store is the same as one that is already there, the **Add** method deletes the existing certificate from the store and then adds the new certificate.</span></span> <span data-ttu-id="37b91-121">Le nouveau certificat hérite des propriétés du certificat existant.</span><span class="sxs-lookup"><span data-stu-id="37b91-121">The new certificate inherits properties from the existing certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b91-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37b91-122">Requirements</span></span>



| <span data-ttu-id="37b91-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37b91-123">Requirement</span></span> | <span data-ttu-id="37b91-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="37b91-124">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37b91-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="37b91-125">Redistributable</span></span><br/> | <span data-ttu-id="37b91-126">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="37b91-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="37b91-127">DLL</span><span class="sxs-lookup"><span data-stu-id="37b91-127">DLL</span></span><br/>             | <dl> <span data-ttu-id="37b91-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37b91-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b91-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37b91-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b91-130">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="37b91-130">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="37b91-131">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="37b91-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
