---
description: Les fonctions suivantes font partie des fonctions CryptoAPI qui peuvent être étendues.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Création de la nouvelle fonctionnalité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525737"
---
# <a name="creating-the-new-functionality"></a><span data-ttu-id="2c023-103">Création de la nouvelle fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="2c023-103">Creating the New Functionality</span></span>

<span data-ttu-id="2c023-104">Les fonctions suivantes font partie des fonctions CryptoAPI qui peuvent être étendues.</span><span class="sxs-lookup"><span data-stu-id="2c023-104">The following functions are among the CryptoAPI functions that can be extended.</span></span>



| <span data-ttu-id="2c023-105">CryptoAPI, fonction</span><span class="sxs-lookup"><span data-stu-id="2c023-105">CryptoAPI function</span></span>                                   | <span data-ttu-id="2c023-106">Nom de la fonction OID define</span><span class="sxs-lookup"><span data-stu-id="2c023-106">OID function name define</span></span>                         | <span data-ttu-id="2c023-107">Chaîne de nom de la fonction OID</span><span class="sxs-lookup"><span data-stu-id="2c023-107">OID function name string</span></span>  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="2c023-108">**CryptEncodeObject**</span><span class="sxs-lookup"><span data-stu-id="2c023-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | <span data-ttu-id="2c023-109">chiffrer l' \_ \_ \_ objet \_ Func OID encode</span><span class="sxs-lookup"><span data-stu-id="2c023-109">CRYPT\_OID\_ENCODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="2c023-110">"CryptDllEncodeObject"</span><span class="sxs-lookup"><span data-stu-id="2c023-110">"CryptDllEncodeObject"</span></span>    |
| [<span data-ttu-id="2c023-111">**CryptDecodeObject**</span><span class="sxs-lookup"><span data-stu-id="2c023-111">**CryptDecodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | <span data-ttu-id="2c023-112">CRYPT \_ OID \_ décoder l' \_ objet \_ Func</span><span class="sxs-lookup"><span data-stu-id="2c023-112">CRYPT\_OID\_DECODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="2c023-113">"CryptDllDecodeObject"</span><span class="sxs-lookup"><span data-stu-id="2c023-113">"CryptDllDecodeObject"</span></span>    |
| [<span data-ttu-id="2c023-114">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="2c023-114">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | <span data-ttu-id="2c023-115">chiffrer le \_ \_ magasin Open OID Open \_ Store \_ \_</span><span class="sxs-lookup"><span data-stu-id="2c023-115">CRYPT\_OID\_OPEN\_ STORE\_PROV\_FUNC</span></span><br/>  | <span data-ttu-id="2c023-116">"CertDllOpenStoreProv"</span><span class="sxs-lookup"><span data-stu-id="2c023-116">"CertDllOpenStoreProv"</span></span>    |
| [<span data-ttu-id="2c023-117">**CertVerifyCTLUsage**</span><span class="sxs-lookup"><span data-stu-id="2c023-117">**CertVerifyCTLUsage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | <span data-ttu-id="2c023-118">CRYPT \_ OID \_ - \_ vérifier \_ l’utilisation de la liste CTL \_</span><span class="sxs-lookup"><span data-stu-id="2c023-118">CRYPT\_OID\_VERIFY\_ CTL\_USAGE\_FUNC</span></span><br/> | <span data-ttu-id="2c023-119">"CertDllVerifyCTLUsage"</span><span class="sxs-lookup"><span data-stu-id="2c023-119">"CertDllVerifyCTLUsage"</span></span>   |
| [<span data-ttu-id="2c023-120">**CertVerifyRevocation**</span><span class="sxs-lookup"><span data-stu-id="2c023-120">**CertVerifyRevocation**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | <span data-ttu-id="2c023-121">chiffrer la vérification de la \_ \_ \_ révocation des OID \_</span><span class="sxs-lookup"><span data-stu-id="2c023-121">CRYPT\_OID\_VERIFY\_ REVOCATION\_FUNC</span></span><br/> | <span data-ttu-id="2c023-122">"CertDllVerifyRevocation"</span><span class="sxs-lookup"><span data-stu-id="2c023-122">"CertDllVerifyRevocation"</span></span> |



 

<span data-ttu-id="2c023-123">En mode d’utilisation normale avec un OID et un type d’encodage existants, le code de la fonction CryptoAPI, lui-même, est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2c023-123">In normal use with an existing OID and encoding type, the code in the CryptoAPI function, itself, is used.</span></span> <span data-ttu-id="2c023-124">Si l’une de ces fonctions est appelée avec un OID et que le type d’encodage n’a pas été conçu pour gérer le code de la fonction CryptoAPI, une nouvelle fonction, contenant les nouvelles fonctionnalités, doit être créée dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="2c023-124">If one of these functions is called with an OID and encoding type that code in the CryptoAPI function was not designed to handle, a new function, containing the new functionality, must be created in a DLL.</span></span> <span data-ttu-id="2c023-125">Cette DLL doit être inscrite dans le registre ou installée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="2c023-125">That DLL must be registered in the registry or installed in memory.</span></span>

<span data-ttu-id="2c023-126">Lorsque l’une des fonctions répertoriées est appelée avec l’OID et le type d’encodage récemment désignés, le code de la nouvelle DLL est utilisé au lieu du code fourni dans le cadre de la fonction CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="2c023-126">When one of the listed functions is called with the newly designated OID and encoding type, the code in the new DLL is used rather than the code provided as part of the CryptoAPI function.</span></span>

<span data-ttu-id="2c023-127">Le nom de la fonction nouvellement développée peut être le nom répertorié sous « OID Function name string » dans le tableau précédent, ou un autre nom peut être donné lorsque le nouveau code de la fonction est inscrit.</span><span class="sxs-lookup"><span data-stu-id="2c023-127">The name of the newly developed function can be the name listed under "OID function name string" in the previous table or a different name can be given when the new function code is registered.</span></span>

<span data-ttu-id="2c023-128">La nouvelle fonction doit utiliser un prototype approprié.</span><span class="sxs-lookup"><span data-stu-id="2c023-128">The new function must use an appropriate prototype.</span></span> <span data-ttu-id="2c023-129">Dans tous les cas, à l’exception de [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), ce prototype est le même que la fonction CryptoAPI qui appelle la nouvelle fonction.</span><span class="sxs-lookup"><span data-stu-id="2c023-129">In all cases except for [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), this prototype is the same as the CryptoAPI function that calls the new function.</span></span> <span data-ttu-id="2c023-130">Dans le cas de **CertOpenStore** , le prototype est le suivant.</span><span class="sxs-lookup"><span data-stu-id="2c023-130">In the case of **CertOpenStore** the prototype is as follows.</span></span>


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> <span data-ttu-id="2c023-131">Si les prototypes ne correspondent pas, la pile système est endommagée.</span><span class="sxs-lookup"><span data-stu-id="2c023-131">If the prototypes do not match, the system stack will be corrupted.</span></span>

 

<span data-ttu-id="2c023-132">En plus de fournir le code de la nouvelle fonction dans une DLL, l’extension de la fonctionnalité de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) ou [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) nécessite la définition d’une définition de type pour que la nouvelle structure de données C soit placée dans un fichier d’en-tête inclus lorsque le programme de l’utilisateur est compilé.</span><span class="sxs-lookup"><span data-stu-id="2c023-132">In addition to providing the code for the new function in a DLL, extending the functionality of [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) or [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requires a type definition for the new C data structure to be placed in a header file included when the user's program is compiled.</span></span>

 

 




