---
title: Utilisation d’un objet de données ActiveX pour la liaison aux fournisseurs ADSI
description: Étant donné qu’ADSI est également un fournisseur OLE DB, vous pouvez utiliser un objet ADO (ActiveX Data Object) pour vous connecter aux fournisseurs ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX Data Object ADSI
- ActiveX Data Object ADSI, utilisation d’ADO pour établir une liaison avec des fournisseurs ADSI
- fournisseurs de services ADSI, utilisation de l’objet de données ActiveX pour la liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028543"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a><span data-ttu-id="ccf52-106">Utilisation d’un objet de données ActiveX pour la liaison aux fournisseurs ADSI</span><span class="sxs-lookup"><span data-stu-id="ccf52-106">Using an ActiveX Data Object to Bind to ADSI Providers</span></span>

<span data-ttu-id="ccf52-107">Étant donné qu’ADSI est également un fournisseur OLE DB, vous pouvez utiliser un objet ADO (ActiveX Data Object) pour vous connecter aux fournisseurs ADSI.</span><span class="sxs-lookup"><span data-stu-id="ccf52-107">Since ADSI is also an OLE DB provider, you can use an ActiveX Data Object (ADO) to connect to ADSI providers.</span></span> <span data-ttu-id="ccf52-108">Comme avec les autres fournisseurs ADO, pour vous connecter à un fournisseur de OLE DB, vous devez créer un objet de connexion et, éventuellement, spécifier les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="ccf52-108">As with other ADO providers, to connect to an OLE DB provider, you must create a new connection object and, optionally, specify the credentials.</span></span> <span data-ttu-id="ccf52-109">Le nom du fournisseur d’OLE DB ADSI est **ADSDSOObject**.</span><span class="sxs-lookup"><span data-stu-id="ccf52-109">The name of the ADSI OLE DB provider is **ADsDSOObject**.</span></span>

<span data-ttu-id="ccf52-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ccf52-110">For example:</span></span>


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



<span data-ttu-id="ccf52-111">Dans l’exemple précédent, vous êtes connecté pour le compte de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="ccf52-111">In the previous example, you are connected on behalf of the current user.</span></span> <span data-ttu-id="ccf52-112">Pour spécifier des informations d’identification différentes, utilisez les propriétés de connexion :</span><span class="sxs-lookup"><span data-stu-id="ccf52-112">To specify different credentials, use connection properties:</span></span>


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



<span data-ttu-id="ccf52-113">ADSI OLE DB définit les propriétés de connexion suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccf52-113">ADSI OLE DB defines the following connection properties.</span></span>



| <span data-ttu-id="ccf52-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="ccf52-114">Property</span></span>           | <span data-ttu-id="ccf52-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccf52-115">Data type</span></span>   | <span data-ttu-id="ccf52-116">Default</span><span class="sxs-lookup"><span data-stu-id="ccf52-116">Default</span></span>   |
|--------------------|-------------|-----------|
| <span data-ttu-id="ccf52-117">« ID utilisateur »</span><span class="sxs-lookup"><span data-stu-id="ccf52-117">"User ID"</span></span>          | <span data-ttu-id="ccf52-118">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="ccf52-118">**BSTR**</span></span>    | <span data-ttu-id="ccf52-119">**NULL**</span><span class="sxs-lookup"><span data-stu-id="ccf52-119">**NULL**</span></span>  |
| <span data-ttu-id="ccf52-120">« Mot de passe »</span><span class="sxs-lookup"><span data-stu-id="ccf52-120">"Password"</span></span>         | <span data-ttu-id="ccf52-121">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="ccf52-121">**BSTR**</span></span>    | <span data-ttu-id="ccf52-122">**NULL**</span><span class="sxs-lookup"><span data-stu-id="ccf52-122">**NULL**</span></span>  |
| <span data-ttu-id="ccf52-123">« Chiffrer le mot de passe »</span><span class="sxs-lookup"><span data-stu-id="ccf52-123">"Encrypt Password"</span></span> | <span data-ttu-id="ccf52-124">**EXPRESSION**</span><span class="sxs-lookup"><span data-stu-id="ccf52-124">**BOOLEAN**</span></span> | <span data-ttu-id="ccf52-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ccf52-125">**FALSE**</span></span> |
| <span data-ttu-id="ccf52-126">« Indicateur ADSI »</span><span class="sxs-lookup"><span data-stu-id="ccf52-126">"ADSI Flag"</span></span>        | <span data-ttu-id="ccf52-127">**Long**</span><span class="sxs-lookup"><span data-stu-id="ccf52-127">**Long**</span></span>    | <span data-ttu-id="ccf52-128">0</span><span class="sxs-lookup"><span data-stu-id="ccf52-128">0</span></span>         |



 

<span data-ttu-id="ccf52-129">En utilisant OLE DB ADO, vous ne pouvez pas lier à un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="ccf52-129">Using OLE DB ADO, you cannot bind to a specific object.</span></span> <span data-ttu-id="ccf52-130">Toutefois, vous pouvez interroger un objet spécifique et obtenir un jeu de résultats en retour.</span><span class="sxs-lookup"><span data-stu-id="ccf52-130">You can, however, query a specific object and get a result set back.</span></span> <span data-ttu-id="ccf52-131">Seuls les fournisseurs ADSI qui prennent en charge le service [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) bénéficient d’un modèle de programmation ADO.</span><span class="sxs-lookup"><span data-stu-id="ccf52-131">Only ADSI providers that support [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefit from having ADO as a programming model.</span></span>

<span data-ttu-id="ccf52-132">La propriété indicateur ADSI est utilisée pour spécifier l’option d’authentification de liaison.</span><span class="sxs-lookup"><span data-stu-id="ccf52-132">The ADSI Flag property is used to specify the binding authentication option.</span></span> <span data-ttu-id="ccf52-133">Cette propriété peut être une combinaison d’indicateurs de l’énumération d’énumération [**\_ d' \_ authentification ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .</span><span class="sxs-lookup"><span data-stu-id="ccf52-133">This property can be a combination of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration.</span></span>

 

 




