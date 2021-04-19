---
description: La méthode Remove supprime un certificat d’un magasin de certificats ouvert. Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove (méthode)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528084"
---
# <a name="storeremove-method"></a><span data-ttu-id="d1db0-104">Store. Remove (méthode)</span><span class="sxs-lookup"><span data-stu-id="d1db0-104">Store.Remove method</span></span>

<span data-ttu-id="d1db0-105">\[La méthode **Remove** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d1db0-105">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d1db0-106">Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d1db0-106">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d1db0-107">La méthode **Remove** supprime un [*certificat*](../secgloss/c-gly.md) d’un [*magasin de certificats*](../secgloss/c-gly.md)ouvert.</span><span class="sxs-lookup"><span data-stu-id="d1db0-107">The **Remove** method removes a [*certificate*](../secgloss/c-gly.md) from an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d1db0-108">Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d1db0-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1db0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1db0-109">Syntax</span></span>


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="d1db0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1db0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1db0-111">*Certificat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1db0-111">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1db0-112">Expression qui correspond à une instance d’un objet de [**certificat**](certificate.md) à supprimer du magasin.</span><span class="sxs-lookup"><span data-stu-id="d1db0-112">Expression that resolves to an instance of a [**Certificate**](certificate.md) object to be removed from the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1db0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1db0-113">Return value</span></span>

<span data-ttu-id="d1db0-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d1db0-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1db0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d1db0-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1db0-116">Lorsque cette méthode est appelée à partir d’un script Web, le script doit supprimer des certificats numériques de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d1db0-116">When this method is called from a web script, the script needs to delete digital certificates from the local computer.</span></span> <span data-ttu-id="d1db0-117">Autoriser les sites Web non approuvés à supprimer des certificats numériques est un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="d1db0-117">Allowing untrusted websites to delete digital certificates is a security risk.</span></span> <span data-ttu-id="d1db0-118">Une boîte de dialogue qui vous demande si le site Web peut supprimer des certificats apparaît lorsque cette méthode est appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="d1db0-118">A dialog box that asks whether the website can delete certificates appears when this method is first called.</span></span> <span data-ttu-id="d1db0-119">Si vous autorisez l’application à supprimer des certificats et que vous sélectionnez ne plus afficher cette boîte de dialogue, la boîte de dialogue n’apparaît plus pour les scripts qui suppriment les certificats dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="d1db0-119">If you allow the application to delete certificates and select "Do not show this dialog box again," the dialog box will no longer appear for any script that deletes certificates within that domain.</span></span> <span data-ttu-id="d1db0-120">Toutefois, les scripts en dehors de ce domaine qui tentent de supprimer des certificats entraînent l’affichage de cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d1db0-120">However, scripts outside that domain that attempt to delete certificates will still cause this dialog box to appear.</span></span> <span data-ttu-id="d1db0-121">Si vous n’autorisez pas le script à supprimer des certificats et que vous sélectionnez ne plus afficher cette boîte de dialogue, les scripts de ce domaine ne seront pas autorisés à supprimer des certificats.</span><span class="sxs-lookup"><span data-stu-id="d1db0-121">If you do not allow the script to delete certificates and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to delete certificates.</span></span>

 

<span data-ttu-id="d1db0-122">Lorsque vous supprimez un certificat d’un magasin, vous devez d’abord supprimer la clé privée associée au certificat.</span><span class="sxs-lookup"><span data-stu-id="d1db0-122">When you delete a certificate from a store, you should first delete the private key associated with the certificate.</span></span>

<span data-ttu-id="d1db0-123">Si le magasin n’est pas ouvert avec l’autorisation de lecture/écriture, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="d1db0-123">If the store is not open with read/write permission, this method fails.</span></span> <span data-ttu-id="d1db0-124">Bien que cette méthode puisse être utilisée avec les magasins de mémoire, toute modification apportée à un magasin de mémoire n’est pas conservée lors de la fermeture de la Banque.</span><span class="sxs-lookup"><span data-stu-id="d1db0-124">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1db0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1db0-125">Requirements</span></span>



| <span data-ttu-id="d1db0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1db0-126">Requirement</span></span> | <span data-ttu-id="d1db0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1db0-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1db0-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d1db0-128">Redistributable</span></span><br/> | <span data-ttu-id="d1db0-129">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1db0-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d1db0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d1db0-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="d1db0-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1db0-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1db0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1db0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1db0-133">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="d1db0-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="d1db0-134">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="d1db0-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
