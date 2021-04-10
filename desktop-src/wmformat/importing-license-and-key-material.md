---
title: Importation de la licence et du matériel de clé
description: Importation de la licence et du matériel de clé
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), matériel de clé
- DRM (gestion des droits numériques), matériel de clé
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, matériel de clé
- API étendues du client, matériel de clé
- licences, importation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197319"
---
# <a name="importing-license-and-key-material"></a>Importation de la licence et du matériel de clé

Si vous avez un contenu multimédia qui a été chiffré à l’aide d’un système de protection de contenu tiers et que vous souhaitez importer la licence et le matériel de clé dans Windows Media DRM, procédez comme suit :

1.  Récupérez la collection de certificats de l’ordinateur Windows Media DRM en appelant la méthode [**IWMDRMSecurity :: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .
2.  Analysez la collection de certificats, en vous assurant qu’elle est correctement signée et qu’elle est validée avec une clé publique racine Microsoft connue. La collection de certificats est conforme au schéma XMR. Pour plus d’informations, consultez [génération d’une licence XMR](building-an-xmr-license.md).
3.  Facultatif : extrayez la liste de révocation en appelant la méthode [**IWMDRMSecurity :: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
4.  Facultatif : Assurez-vous qu’aucun certificat de la collection n’est révoqué. Pour plus d’informations, consultez vérification de la [révocation des certificats](checking-certificate-revocation.md).
5.  Générez une licence au format XMR qui représente les spécifications de la stratégie pour le contenu d’importation et qui contient le matériel de clé DRM Windows Media approprié. Pour plus d’informations, consultez la rubrique [création d’une licence XMR](building-an-xmr-license.md).
6.  Transmettez la licence XMR au système Windows Media DRM en vue de son traitement, à l’aide de la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

> [!Note]  
> Des informations sur le schéma XMR vous seront fournies lors de la licence de Windows Media DRM.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vérification de la révocation des certificats**](checking-certificate-revocation.md)
</dt> <dt>

[**Génération d’une licence XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importation DRM**](drm-import.md)
</dt> </dl>

 

 




