---
description: Un magasin système est un regroupement qui se compose d’un ou de plusieurs magasins frères physiques.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Emplacements du magasin système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952115"
---
# <a name="system-store-locations"></a><span data-ttu-id="ad73c-103">Emplacements du magasin système</span><span class="sxs-lookup"><span data-stu-id="ad73c-103">System Store Locations</span></span>

<span data-ttu-id="ad73c-104">Un magasin système est un regroupement qui se compose d’un ou de plusieurs magasins frères physiques.</span><span class="sxs-lookup"><span data-stu-id="ad73c-104">A system store is a collection that consists of one or more physical sibling stores.</span></span> <span data-ttu-id="ad73c-105">Pour chaque magasin système, il existe des magasins frères physiques prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="ad73c-105">For each system store, there are predefined physical sibling stores.</span></span> <span data-ttu-id="ad73c-106">Après l’ouverture d’un magasin système comme MY at CERT \_ System \_ Store \_ Current \_ User, le fournisseur Store appelle [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) pour ouvrir chacun des magasins physiques dans le regroupement du magasin système.</span><span class="sxs-lookup"><span data-stu-id="ad73c-106">After opening a system store such as MY at CERT\_SYSTEM\_STORE\_CURRENT\_USER, the store provider calls [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open each of the physical stores in the system store collection.</span></span> <span data-ttu-id="ad73c-107">Dans le processus ouvert, chacun de ces magasins physiques est ajouté au regroupement du magasin système à l’aide de [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span><span class="sxs-lookup"><span data-stu-id="ad73c-107">In the open process, each of these physical stores is added to the system store collection using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span> <span data-ttu-id="ad73c-108">Tous les certificats de ces magasins physiques sont disponibles par le biais du regroupement du magasin de système logique.</span><span class="sxs-lookup"><span data-stu-id="ad73c-108">All certificates in those physical stores are available through the logical system store collection.</span></span>

<span data-ttu-id="ad73c-109">Pour chaque emplacement du magasin système, les magasins de systèmes prédéfinis sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ad73c-109">For each system store location, the predefined systems stores are:</span></span>

-   <span data-ttu-id="ad73c-110">MY</span><span class="sxs-lookup"><span data-stu-id="ad73c-110">MY</span></span>
-   <span data-ttu-id="ad73c-111">Root</span><span class="sxs-lookup"><span data-stu-id="ad73c-111">Root</span></span>
-   <span data-ttu-id="ad73c-112">Confiance</span><span class="sxs-lookup"><span data-stu-id="ad73c-112">Trust</span></span>
-   <span data-ttu-id="ad73c-113">CA</span><span class="sxs-lookup"><span data-stu-id="ad73c-113">CA</span></span>

<span data-ttu-id="ad73c-114">Dans l' \_ \_ utilisateur actuel du magasin système CERT \_ \_ , il existe également un magasin UserDS prédéfini.</span><span class="sxs-lookup"><span data-stu-id="ad73c-114">In CERT\_SYSTEM\_STORE\_CURRENT\_USER, there is also a predefined UserDS store.</span></span> <span data-ttu-id="ad73c-115">Un magasin de cartes à puce est prévu pour cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="ad73c-115">A smart card store is planned for this location.</span></span>

<span data-ttu-id="ad73c-116">Voici les magasins système suivis par d’autres remarques :</span><span class="sxs-lookup"><span data-stu-id="ad73c-116">Here are the system stores followed by further remarks:</span></span>

-   [<span data-ttu-id="ad73c-117">\_magasin système du certificat \_ \_ \_ utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="ad73c-117">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>](#cert_system_store_current_user)
-   [<span data-ttu-id="ad73c-118">\_ \_ ordinateur local du magasin système \_ du \_ certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-118">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>](#cert_system_store_local_machine)
-   [<span data-ttu-id="ad73c-119">\_service du magasin système du certificat \_ \_ actuel \_</span><span class="sxs-lookup"><span data-stu-id="ad73c-119">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>](#cert_system_store_current_service)
-   [<span data-ttu-id="ad73c-120">\_services du \_ magasin \_ système du certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-120">CERT\_SYSTEM\_STORE\_SERVICES</span></span>](#cert_system_store_services)
-   [<span data-ttu-id="ad73c-121">\_utilisateurs du \_ magasin \_ système du certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-121">CERT\_SYSTEM\_STORE\_USERS</span></span>](#cert_system_store_users)
-   [<span data-ttu-id="ad73c-122">stratégie de groupe de l' \_ \_ utilisateur actuel du système CERT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad73c-122">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>](#cert_system_current_user_group_policy)
-   [<span data-ttu-id="ad73c-123">stratégie de groupe de l' \_ \_ ordinateur local du système CERT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad73c-123">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>](#cert_system_local_machine_group_policy)
-   [<span data-ttu-id="ad73c-124">CERT \_ System \_ Store \_ local \_ machine \_ Enterprise</span><span class="sxs-lookup"><span data-stu-id="ad73c-124">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>](#cert_system_store_local_machine_enterprise)
-   [<span data-ttu-id="ad73c-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad73c-125">Remarks</span></span>](#remarks)

### <a name="cert_system_store_current_user"></a><span data-ttu-id="ad73c-126">\_magasin système du certificat \_ \_ \_ utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="ad73c-126">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>

<span data-ttu-id="ad73c-127">\_Magasin système de certificats \_ \_ \_ les magasins système de l’utilisateur actuel se trouvent à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ad73c-127">CERT\_SYSTEM\_STORE\_CURRENT\_USER system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="ad73c-128">Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ad73c-128">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="ad73c-129">Magasin système</span><span class="sxs-lookup"><span data-stu-id="ad73c-129">System store</span></span> | <span data-ttu-id="ad73c-130">Magasin physique</span><span class="sxs-lookup"><span data-stu-id="ad73c-130">Physical store</span></span>                                           |
|--------------|----------------------------------------------------------|
| <span data-ttu-id="ad73c-131">MY</span><span class="sxs-lookup"><span data-stu-id="ad73c-131">MY</span></span>           | <span data-ttu-id="ad73c-132">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-132">.Default</span></span>                                                 |
| <span data-ttu-id="ad73c-133">Root</span><span class="sxs-lookup"><span data-stu-id="ad73c-133">Root</span></span>         | <span data-ttu-id="ad73c-134">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-134">.Default.LocalMachine</span></span><br/> <span data-ttu-id="ad73c-135">. Carte à puce</span><span class="sxs-lookup"><span data-stu-id="ad73c-135">.SmartCard</span></span><br/>   |
| <span data-ttu-id="ad73c-136">Confiance</span><span class="sxs-lookup"><span data-stu-id="ad73c-136">Trust</span></span>        | <span data-ttu-id="ad73c-137">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="ad73c-137">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="ad73c-138">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-138">.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-139">CA</span><span class="sxs-lookup"><span data-stu-id="ad73c-139">CA</span></span>           | <span data-ttu-id="ad73c-140">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="ad73c-140">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="ad73c-141">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-141">.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-142">UserDS</span><span class="sxs-lookup"><span data-stu-id="ad73c-142">UserDS</span></span>       | <span data-ttu-id="ad73c-143">. UserCertificate</span><span class="sxs-lookup"><span data-stu-id="ad73c-143">.UserCertificate</span></span>                                         |



 

### <a name="cert_system_store_local_machine"></a><span data-ttu-id="ad73c-144">\_ \_ ordinateur local du magasin système \_ du \_ certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-144">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>

<span data-ttu-id="ad73c-145">\_ \_ \_ \_ Les magasins du système de l’ordinateur local du magasin système du certificat se trouvent à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ad73c-145">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="ad73c-146">Les magasins physiques prédéfinis sont associés à ces magasins système, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ad73c-146">The predefined physical stores are associated with those system stores are as follows.</span></span>



| <span data-ttu-id="ad73c-147">Magasin système</span><span class="sxs-lookup"><span data-stu-id="ad73c-147">System store</span></span> | <span data-ttu-id="ad73c-148">Magasin physique</span><span class="sxs-lookup"><span data-stu-id="ad73c-148">Physical store</span></span>                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad73c-149">MY</span><span class="sxs-lookup"><span data-stu-id="ad73c-149">MY</span></span>           | <span data-ttu-id="ad73c-150">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-150">.Default</span></span>                                                                                          |
| <span data-ttu-id="ad73c-151">Root</span><span class="sxs-lookup"><span data-stu-id="ad73c-151">Root</span></span>         | <span data-ttu-id="ad73c-152">. Default. AuthRoot</span><span class="sxs-lookup"><span data-stu-id="ad73c-152">.Default.AuthRoot</span></span><br/> <span data-ttu-id="ad73c-153">. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="ad73c-153">.GroupPolicy</span></span><br/> <span data-ttu-id="ad73c-154">. Entreprise</span><span class="sxs-lookup"><span data-stu-id="ad73c-154">.Enterprise</span></span><br/> <span data-ttu-id="ad73c-155">. Carte à puce</span><span class="sxs-lookup"><span data-stu-id="ad73c-155">.SmartCard</span></span><br/> |
| <span data-ttu-id="ad73c-156">Confiance</span><span class="sxs-lookup"><span data-stu-id="ad73c-156">Trust</span></span>        | <span data-ttu-id="ad73c-157">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="ad73c-157">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="ad73c-158">. Entreprise</span><span class="sxs-lookup"><span data-stu-id="ad73c-158">.Enterprise</span></span><br/>                                            |
| <span data-ttu-id="ad73c-159">CA</span><span class="sxs-lookup"><span data-stu-id="ad73c-159">CA</span></span>           | <span data-ttu-id="ad73c-160">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="ad73c-160">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="ad73c-161">. Entreprise</span><span class="sxs-lookup"><span data-stu-id="ad73c-161">.Enterprise</span></span> <br/>                                           |



 

### <a name="cert_system_store_current_service"></a><span data-ttu-id="ad73c-162">\_service du magasin système du certificat \_ \_ actuel \_</span><span class="sxs-lookup"><span data-stu-id="ad73c-162">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>

<span data-ttu-id="ad73c-163">\_ \_ \_ \_ Les magasins du système de service du magasin système du certificat actuel se trouvent à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ad73c-163">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="ad73c-164">Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ad73c-164">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="ad73c-165">Magasin système</span><span class="sxs-lookup"><span data-stu-id="ad73c-165">System store</span></span> | <span data-ttu-id="ad73c-166">Magasin physique</span><span class="sxs-lookup"><span data-stu-id="ad73c-166">Physical store</span></span>                   |
|--------------|----------------------------------|
| <span data-ttu-id="ad73c-167">MY</span><span class="sxs-lookup"><span data-stu-id="ad73c-167">MY</span></span>           | <span data-ttu-id="ad73c-168">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-168">.Default</span></span>                         |
| <span data-ttu-id="ad73c-169">Root</span><span class="sxs-lookup"><span data-stu-id="ad73c-169">Root</span></span>         | <span data-ttu-id="ad73c-170">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-170">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-171">Confiance</span><span class="sxs-lookup"><span data-stu-id="ad73c-171">Trust</span></span>        | <span data-ttu-id="ad73c-172">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-172">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-173">CA</span><span class="sxs-lookup"><span data-stu-id="ad73c-173">CA</span></span>           | <span data-ttu-id="ad73c-174">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-174">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_services"></a><span data-ttu-id="ad73c-175">\_services du \_ magasin \_ système du certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-175">CERT\_SYSTEM\_STORE\_SERVICES</span></span>

<span data-ttu-id="ad73c-176">\_ \_ \_ Les magasins système des services du magasin système de certificats se trouvent à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ad73c-176">CERT\_SYSTEM\_STORE\_SERVICES system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="ad73c-177">Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ad73c-177">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="ad73c-178">Magasin système</span><span class="sxs-lookup"><span data-stu-id="ad73c-178">System store</span></span>       | <span data-ttu-id="ad73c-179">Magasin physique</span><span class="sxs-lookup"><span data-stu-id="ad73c-179">Physical store</span></span>                   |
|--------------------|----------------------------------|
| <span data-ttu-id="ad73c-180">ServiceName \\ My</span><span class="sxs-lookup"><span data-stu-id="ad73c-180">ServiceName\\MY</span></span>    | <span data-ttu-id="ad73c-181">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-181">.Default</span></span>                         |
| <span data-ttu-id="ad73c-182">\\Racine ServiceName</span><span class="sxs-lookup"><span data-stu-id="ad73c-182">ServiceName\\Root</span></span>  | <span data-ttu-id="ad73c-183">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-183">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-184">\\Confiance ServiceName</span><span class="sxs-lookup"><span data-stu-id="ad73c-184">ServiceName\\Trust</span></span> | <span data-ttu-id="ad73c-185">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-185">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-186">\\AC ServiceName</span><span class="sxs-lookup"><span data-stu-id="ad73c-186">ServiceName\\CA</span></span>    | <span data-ttu-id="ad73c-187">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-187">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_users"></a><span data-ttu-id="ad73c-188">\_utilisateurs du \_ magasin \_ système du certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-188">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="ad73c-189">\_ \_ \_ Les magasins système des utilisateurs du magasin système du certificat se trouvent à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ad73c-189">CERT\_SYSTEM\_STORE\_USERS system stores are at the following registry location:</span></span>

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

<span data-ttu-id="ad73c-190">Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ad73c-190">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="ad73c-191">Magasin système</span><span class="sxs-lookup"><span data-stu-id="ad73c-191">System store</span></span>  | <span data-ttu-id="ad73c-192">Magasin physique</span><span class="sxs-lookup"><span data-stu-id="ad73c-192">Physical store</span></span>                   |
|---------------|----------------------------------|
| <span data-ttu-id="ad73c-193">userid \\ My</span><span class="sxs-lookup"><span data-stu-id="ad73c-193">userid\\MY</span></span>    | <span data-ttu-id="ad73c-194">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-194">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-195">\\racine userid</span><span class="sxs-lookup"><span data-stu-id="ad73c-195">userid\\Root</span></span>  | <span data-ttu-id="ad73c-196">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-196">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-197">\\confiance userid</span><span class="sxs-lookup"><span data-stu-id="ad73c-197">userid\\Trust</span></span> | <span data-ttu-id="ad73c-198">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-198">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="ad73c-199">ID de l' \\ autorité de certification</span><span class="sxs-lookup"><span data-stu-id="ad73c-199">userid\\CA</span></span>    | <span data-ttu-id="ad73c-200">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="ad73c-200">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_current_user_group_policy"></a><span data-ttu-id="ad73c-201">stratégie de groupe de l' \_ \_ utilisateur actuel du système CERT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad73c-201">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>

<span data-ttu-id="ad73c-202">\_Système de \_ certificats \_ \_ \_ les banques système de la stratégie de groupe de l’utilisateur actuel se trouvent à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ad73c-202">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a><span data-ttu-id="ad73c-203">stratégie de groupe de l' \_ \_ ordinateur local du système CERT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad73c-203">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>

<span data-ttu-id="ad73c-204">\_ \_ \_ \_ \_ Les banques système de la stratégie de groupe de l’ordinateur local du certificat se trouvent à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ad73c-204">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a><span data-ttu-id="ad73c-205">CERT \_ System \_ Store \_ local \_ machine \_ Enterprise</span><span class="sxs-lookup"><span data-stu-id="ad73c-205">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>

<span data-ttu-id="ad73c-206">CERT \_ System \_ Store \_ local \_ machine \_ Enterprise contient les certificats partagés entre les domaines de l’entreprise et téléchargés à partir de l’annuaire global de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ad73c-206">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE contains certificates shared across domains in the enterprise and downloaded from the global enterprise directory.</span></span> <span data-ttu-id="ad73c-207">Pour synchroniser le magasin de l’entreprise du client, l’annuaire d’entreprise est interrogé toutes les huit heures et les certificats sont téléchargés automatiquement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ad73c-207">To synchronize the client's enterprise store, the enterprise directory is polled every eight hours and certificates are downloaded automatically in the background.</span></span>

<span data-ttu-id="ad73c-208">Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ad73c-208">The predefined physical stores associated with these system stores are as follows.</span></span>



| <span data-ttu-id="ad73c-209">Magasin système</span><span class="sxs-lookup"><span data-stu-id="ad73c-209">System store</span></span> | <span data-ttu-id="ad73c-210">Magasin physique</span><span class="sxs-lookup"><span data-stu-id="ad73c-210">Physical store</span></span> |
|--------------|----------------|
| <span data-ttu-id="ad73c-211">MY</span><span class="sxs-lookup"><span data-stu-id="ad73c-211">MY</span></span>           | <span data-ttu-id="ad73c-212">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-212">.Default</span></span>       |
| <span data-ttu-id="ad73c-213">Root</span><span class="sxs-lookup"><span data-stu-id="ad73c-213">Root</span></span>         | <span data-ttu-id="ad73c-214">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-214">.Default</span></span>       |
| <span data-ttu-id="ad73c-215">Confiance</span><span class="sxs-lookup"><span data-stu-id="ad73c-215">Trust</span></span>        | <span data-ttu-id="ad73c-216">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-216">.Default</span></span>       |
| <span data-ttu-id="ad73c-217">CA</span><span class="sxs-lookup"><span data-stu-id="ad73c-217">CA</span></span>           | <span data-ttu-id="ad73c-218">. Valeurs</span><span class="sxs-lookup"><span data-stu-id="ad73c-218">.Default</span></span>       |



 

### <a name="remarks"></a><span data-ttu-id="ad73c-219">Notes</span><span class="sxs-lookup"><span data-stu-id="ad73c-219">Remarks</span></span>

<span data-ttu-id="ad73c-220">Des magasins physiques supplémentaires peuvent être associés à un magasin système à l’aide de [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span><span class="sxs-lookup"><span data-stu-id="ad73c-220">Additional physical stores can be associated with a system store by using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>

<span data-ttu-id="ad73c-221">Les \_ magasins de certificats du magasin système \_ \_ et \_ \_ \_ d’utilisateurs du magasin système du certificat sont ouverts en préfixant le nom du magasin dans la chaîne transmise à *pvPara* avec le nom de service ou d’utilisateur, tel que *ServiceName* \\ **Trust** ou **. Par défaut** \\ **My**.</span><span class="sxs-lookup"><span data-stu-id="ad73c-221">CERT\_SYSTEM\_STORE\_SERVICE and CERT\_SYSTEM\_STORE\_USERS stores are opened by prefixing the name of the store in the string passed to *pvPara* with the service or user name such as *ServiceName*\\**Trust** or **.Default**\\**MY**.</span></span> <span data-ttu-id="ad73c-222">L’emplacement des utilisateurs du magasin du système \_ \_ de certificats \_ ou des services du magasin système de certificats \_ \_ \_ peut ouvrir le même magasin dans le service actuel du système de certificats ou dans le \_ \_ \_ \_ \_ magasin système de certificats de l' \_ utilisateur actuel à \_ l’aide de l' [*identificateur de sécurité*](../secgloss/s-gly.md) textuel (SID) du service ou de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="ad73c-222">The CERT\_SYSTEM\_STORE\_SERVICES or CERT\_SYSTEM\_STORE\_USERS location can open the same store in CERT\_SYSTEM\_CURRENT\_SERVICE or CERT\_SYSTEM\_STORE\_CURRENT\_USER by using the textual [*security identifier*](../secgloss/s-gly.md) (SID) of the current service or user.</span></span>

<span data-ttu-id="ad73c-223">Les magasins dans la stratégie de \_ groupe d’utilisateurs du magasin système du certificat \_ \_ \_ \_ et \_ \_ \_ \_ \_ la stratégie de groupe de l’ordinateur local du système de certificats dans un paramètre réseau sont téléchargés sur l’ordinateur client à partir du modèle de stratégie de groupe (GPT) lors du démarrage de l’ordinateur ou de l’ouverture de session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad73c-223">Stores in CERT\_SYSTEM\_STORE\_USER\_GROUP\_POLICY and CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY in a network setting are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.</span></span> <span data-ttu-id="ad73c-224">Ces magasins peuvent être mis à jour sur l’ordinateur client après le démarrage ou l’ouverture de session lorsque le GPT est modifié sur le serveur de domaine par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="ad73c-224">These stores can be updated on the client computer after startup or logon when the GPT is changed on the domain server by an administrator.</span></span> <span data-ttu-id="ad73c-225">La fonction [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permet à une application d’être avertie lorsque des magasins dans l’un de ces emplacements ont changé.</span><span class="sxs-lookup"><span data-stu-id="ad73c-225">The [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) function allows an application to be notified when stores in either of these locations have changed.</span></span>

<span data-ttu-id="ad73c-226">Les emplacements du magasin système suivants peuvent être ouverts à distance :</span><span class="sxs-lookup"><span data-stu-id="ad73c-226">The following system store locations can be opened remotely:</span></span>

-   <span data-ttu-id="ad73c-227">\_ \_ ordinateur local du magasin système \_ du \_ certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-227">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>
-   <span data-ttu-id="ad73c-228">stratégie de groupe de l' \_ \_ \_ ordinateur local du magasin système \_ \_ du \_ certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-228">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>
-   <span data-ttu-id="ad73c-229">\_services du \_ magasin \_ système du certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-229">CERT\_SYSTEM\_STORE\_SERVICES</span></span>
-   <span data-ttu-id="ad73c-230">\_utilisateurs du \_ magasin \_ système du certificat</span><span class="sxs-lookup"><span data-stu-id="ad73c-230">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="ad73c-231">Les emplacements du magasin système sont ouverts à distance en préfixant le nom du magasin dans la chaîne transmise à *pvPara* par le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ad73c-231">System store locations are opened remotely by prefixing the store name in the string passed to *pvPara* with the computer name.</span></span> <span data-ttu-id="ad73c-232">Voici des exemples de noms de magasins système distants :</span><span class="sxs-lookup"><span data-stu-id="ad73c-232">Examples of remote system store names are:</span></span>

-   <span data-ttu-id="ad73c-233">*Nom de l’ordinateur* \\ **Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="ad73c-233">*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="ad73c-234">\\\\*Nom de l’ordinateur* \\ **Autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="ad73c-234">\\\\*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="ad73c-235">*Nom de l’ordinateur* \\ *ServiceName* \\ Niveau de **confiance**</span><span class="sxs-lookup"><span data-stu-id="ad73c-235">*ComputerName*\\*ServiceName*\\**Trust**</span></span>
-   <span data-ttu-id="ad73c-236">\\\\*Nom de l’ordinateur* \\ *ServiceName* \\ Niveau de **confiance**</span><span class="sxs-lookup"><span data-stu-id="ad73c-236">\\\\*ComputerName*\\*ServiceName*\\**Trust**</span></span>

 

 
