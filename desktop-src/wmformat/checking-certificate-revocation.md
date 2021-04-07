---
title: Vérification de la révocation des certificats
description: Vérification de la révocation des certificats
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, révocation de certificat
- Windows Media Format SDK, révocation de certificats
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), révocation de certificat
- DRM (gestion des droits numériques), révocation de certificat
- gestion des droits numériques (DRM), révocation des certificats
- DRM (gestion des droits numériques), révocation des certificats
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, révocation de certificat
- API étendues clientes, révocation de certificat
- API étendues du client DRM, révocation de certificats
- API étendues clientes, révocation de certificats
- certificats, révocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673022"
---
# <a name="checking-certificate-revocation"></a>Vérification de la révocation des certificats

Lorsque vous importez du contenu dans Windows Media DRM, vous devez vous assurer qu’aucun certificat dans une collection de certificats n’a été révoqué en vérifiant qu’aucun certificat de la collection n’est dans la liste de révocation. La liste de révocation est extraite à l’aide de la méthode [**IWMDRMSecurity :: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .

Vous utilisez ensuite la méthode [**IWMDRMSecurity :: CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) pour vérifier que le certificat n’est pas révoqué.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Importation DRM**](drm-import.md)
</dt> </dl>

 

 




