---
title: Gestion du contenu protégé dans le fournisseur de services
description: Gestion du contenu protégé dans le fournisseur de services
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Gestionnaire de périphériques de média, certificats
- Gestionnaire de périphériques, certificats
- Guide de programmation, certificats
- fournisseurs de services, certificats
- création de fournisseurs de services, certificats
- certificates
- Windows Gestionnaire de périphériques de média, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Guide de programmation, contenu protégé par DRM
- fournisseurs de services, contenu protégé par DRM
- création de fournisseurs de services, contenu protégé par DRM
- Contenu protégé par DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008514"
---
# <a name="handling-protected-content-in-the-service-provider"></a>Gestion du contenu protégé dans le fournisseur de services

vous pouvez créer un fournisseur de services qui peut envoyer du contenu protégé par drm à un appareil basé sur des drm d’appareils mobiles (PDDRM), mais vous ne pouvez pas créer un fournisseur de services qui peut envoyer du contenu protégé par drm à des appareils basés sur Windows Media drm 10 pour les appareils mobiles. Ces appareils utilisent MTP et vous ne pouvez pas créer votre propre fournisseur de services MTP.

La seule étape supplémentaire qu’un fournisseur de services doit effectuer pour envoyer un matériel DRM à un appareil PDDRM consiste à obtenir un certificat/une paire de clés émis par Microsoft. Pour savoir où obtenir ce certificat ou cette clé, consultez [outils de développement](tools-for-development.md) . Les licences émises pour ces appareils seront des licences simplifiées qui prennent uniquement en charge la lecture simple du contenu acheté. ils ne prennent pas en charge les licences d’expiration temporelles. Cette licence sera créée pour vous par le fournisseur de contenu sécurisé (fourni par Microsoft pour les fichiers WMA/WMV) et stockée dans l’en-tête du fichier envoyé au fournisseur de services. Vous n’aurez pas à effectuer d’étapes spéciales pour les fichiers protégés.

une fois le fichier protégé envoyé, Windows Gestionnaire de périphériques de support appellera le fournisseur de services pour demander un fichier de stockage de licence spécial à partir de l’appareil. Windows Le Gestionnaire de périphériques de média ajoute une copie de la nouvelle licence à ce fichier et le renvoie au fournisseur de services pour le renvoyer à l’appareil. Toutefois, même si le fournisseur de services ne parvient pas à trouver ou à retourner ce fichier, il doit toujours être en mesure de lire le fichier protégé à l’aide de la copie de licence dans l’en-tête de fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> <dt>

[**Gestion du contenu protégé**](handling-protected-content.md)
</dt> </dl>

 

 




