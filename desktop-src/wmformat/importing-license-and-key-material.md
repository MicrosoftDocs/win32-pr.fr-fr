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
ms.openlocfilehash: 4c9852102ab282c983488c2e5c35b7187bf0daccb62d347c312d1afb343b60f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702503"
---
# <a name="importing-license-and-key-material"></a>Importation de la licence et du matériel de clé

si vous avez un contenu multimédia qui a été chiffré à l’aide d’un système de protection de contenu tiers et que vous souhaitez importer la licence et le matériel de clé dans Windows DRM media, procédez comme suit :

1.  récupérez la collection de certificats de l’ordinateur Media DRM Windows en appelant la méthode [**IWMDRMSecurity :: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .
2.  Analysez la collection de certificats, en vous assurant qu’elle est correctement signée et qu’elle est validée avec une clé publique racine Microsoft connue. La collection de certificats est conforme au schéma XMR. Pour plus d’informations, consultez [génération d’une licence XMR](building-an-xmr-license.md).
3.  Facultatif : extrayez la liste de révocation en appelant la méthode [**IWMDRMSecurity :: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
4.  Facultatif : Assurez-vous qu’aucun certificat de la collection n’est révoqué. Pour plus d’informations, consultez vérification de la [révocation des certificats](checking-certificate-revocation.md).
5.  générez une licence au format XMR qui représente les spécifications de la stratégie pour le contenu d’importation et qui contient le matériel de clé DRM Media Windows approprié. Pour plus d’informations, consultez la rubrique [création d’une licence XMR](building-an-xmr-license.md).
6.  transmettez la licence XMR au système Windows Media DRM à des fins de traitement, à l’aide de la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

> [!Note]  
> des informations sur le schéma XMR vous seront fournies lors de la licence Windows Media DRM.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vérification de la révocation des certificats**](checking-certificate-revocation.md)
</dt> <dt>

[**Génération d’une licence XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importation DRM**](drm-import.md)
</dt> </dl>

 

 




