---
title: Suppression de la licence
description: Suppression de la licence
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows Media Format SDK, licences
- Windows Media Format SDK, supprimer des licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), suppression de licences
- DRM (gestion des droits numériques), suppression de licences
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, suppression de licences
- API étendues clientes, suppression de licences
- licences, suppression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510827"
---
# <a name="license-deletion"></a><span data-ttu-id="2f19c-114">Suppression de la licence</span><span class="sxs-lookup"><span data-stu-id="2f19c-114">License Deletion</span></span>

<span data-ttu-id="2f19c-115">Toutes les licences tierces créées localement, par exemple via l’importation DRM, peuvent être supprimées en appelant la méthode [**IWMDRMLicenseManagement ::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="2f19c-115">Any third-party licenses created locally, for example through DRM import, can be deleted by calling the [**IWMDRMLicenseManagement::ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) method.</span></span> <span data-ttu-id="2f19c-116">La chaîne que vous transmettez à cette méthode sera une licence XMR qui ressemble à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="2f19c-116">The string you pass to this method will be an XMR license that resembles the following:</span></span>


```C++
<response type="LRB">
  <DATA>
    <LICENSEDATA>
      <DATA>
        <KID>include Key ID here to revoke certain keys</KID>
        <LID>rights ID</LID
        <META>
          <LGPUBKEY>
            <PublicKey>
              <Modulus>base64 encoded public key</Modulus>
              <Exponent>Exponent in network byte order</Exponent>
            </PublicKey>
          </LGPUBKEY>
          <UID>content-owner-specific user ID</UID>
        </META>
      </DATA>
    </LICENSEDATA>
  </DATA>
</response>
```



<span data-ttu-id="2f19c-117">Le champ ID d’utilisateur spécifique au propriétaire (UID) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2f19c-117">The owner specific user ID (UID) field is optional.</span></span> <span data-ttu-id="2f19c-118">Les champs facultatifs ne doivent pas être inclus dans la réponse de la licence si aucune donnée ne leur est associée.</span><span class="sxs-lookup"><span data-stu-id="2f19c-118">Optional fields must not be included in the license response if there is not any data associated with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f19c-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f19c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f19c-120">**Génération d’une licence XMR**</span><span class="sxs-lookup"><span data-stu-id="2f19c-120">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="2f19c-121">**Importation DRM**</span><span class="sxs-lookup"><span data-stu-id="2f19c-121">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="2f19c-122">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="2f19c-122">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




