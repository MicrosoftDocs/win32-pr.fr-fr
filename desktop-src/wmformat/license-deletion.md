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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234648"
---
# <a name="license-deletion"></a>Suppression de la licence

Toutes les licences tierces créées localement, par exemple via l’importation DRM, peuvent être supprimées en appelant la méthode [**IWMDRMLicenseManagement ::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) . La chaîne que vous transmettez à cette méthode sera une licence XMR qui ressemble à ce qui suit :


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



Le champ ID d’utilisateur spécifique au propriétaire (UID) est facultatif. Les champs facultatifs ne doivent pas être inclus dans la réponse de la licence si aucune donnée ne leur est associée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Génération d’une licence XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importation DRM**](drm-import.md)
</dt> <dt>

[**Guide de programmation**](drm-programming-guide.md)
</dt> </dl>

 

 




