---
title: Gestion du contenu protégé
description: Gestion du contenu protégé
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Gestionnaire de périphériques de média, certificats
- Gestionnaire de périphériques, certificats
- applications de bureau, certificats
- fournisseurs de services, certificats
- Guide de programmation, certificats
- certificates
- Windows Gestionnaire de périphériques de média, fournisseur de contenu sécurisé (SCP)
- Gestionnaire de périphériques, fournisseur de contenu sécurisé (SCP)
- applications de bureau, fournisseur de contenu sécurisé (SCP)
- fournisseurs de services, fournisseur de contenu sécurisé (SCP)
- Guide de programmation, fournisseur de contenu sécurisé (SCP)
- fournisseur de contenu sécurisé (SCP)
- SCP (Secure Content Provider)
- Windows Gestionnaire de périphériques de média, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Guide de programmation, contenu protégé par DRM
- applications de bureau, contenu protégé par DRM
- fournisseurs de services, contenu protégé par DRM
- Contenu protégé par DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f06429ba4a8ac24f4ae2ba3823db9380bd4109b04b924e5a081f287b8aaf30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863179"
---
# <a name="handling-protected-content"></a>Gestion du contenu protégé

si vous créez une application ou un fournisseur de services qui consomme du contenu protégé par Windows Media digital rights management (DRM), vous devez disposer d’une paire clé/certificat émise par Microsoft. Pour savoir où obtenir ce certificat, consultez [outils de développement](tools-for-development.md). Si vous n’envisagez pas de gérer le contenu protégé, vous pouvez utiliser la clé factice et le certificat fournis avec ce kit de développement logiciel (SDK) dans un fichier nommé Key. c.

pour tout fichier protégé par la technologie DRM, Windows Media Gestionnaire de périphériques nécessite la présence d’un fournisseur de contenu sécurisé (SCP) pour ce format de fichier. Microsoft fournit un module SCP pour les fichiers WMA et WMV. Si votre application ou fournisseur de services gère le contenu DRM protégé d’un autre format, vous devez fournir votre propre module SCP. Un module SCP est un objet COM qui implémente toutes les [interfaces des fournisseurs de contenu sécurisés](interfaces-for-secure-content-providers.md).

une application peut envoyer du contenu protégé par drm à des appareils basés sur Windows Media drm 10 pour les appareils portables ou sur des drm d’appareils mobiles (PDDRM). Toutefois, vous pouvez uniquement créer un fournisseur de services pour les appareils basés sur PDDRM ; vous ne pouvez pas créer un fournisseur de services pour les appareils basés sur Windows Media DRM 10 pour les appareils mobiles. Ces derniers appareils peuvent uniquement utiliser le fournisseur de services MTP fourni par Microsoft.

Les appareils basés sur PDDRM peuvent uniquement prendre en charge les licences pour le contenu acheté. les licences qui ont des conditions d’expiration de délai sont uniquement prises en charge par les appareils basés sur Windows Media DRM 10 pour les appareils mobiles, qui ont des exigences particulières, telles que l’horloge sécurisée et l’individualisation. Windows Media DRM 10 pour appareils mobiles le kit de développement logiciel (SDK) fournit des détails sur la configuration requise pour prendre en charge la technologie version 10.

Avant d’envoyer du contenu DRM à l’appareil, une application doit vérifier plusieurs éléments :

-   Que l’appareil prend en charge la technologie DRM.
-   La version de la technologie DRM prise en charge (version 10 ou antérieure).
-   Si l’appareil est basé sur la version 10, tous ses composants sont à jour (par exemple, l’horloge sécurisée et toutes les exigences d’individualisation).

tous les appels de méthode pour répondre à ces questions sont faits par le client et gérés par Windows Media Gestionnaire de périphériques et le composant secure content provider. le fournisseur de services ne gère aucun de ces appels.

si l’appareil ne prend pas en charge Windows Media DRM 10 pour les appareils mobiles, il peut toujours être en mesure de consommer du contenu protégé (en fonction de la licence de contenu et de la conception de l’appareil), mais tout contenu qui lui est envoyé disposera d’une licence d’utilisation simplifiée avec des droits limités (par exemple, pas de délai d’expiration).

-   Pour obtenir des exemples montrant comment une application vérifie si un appareil peut gérer du contenu protégé et s’il doit mettre à jour ses composants DRM, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md).
-   Pour plus d’informations sur la création d’un fournisseur de services pouvant gérer du contenu protégé, consultez [gestion du contenu protégé dans le fournisseur de services](handling-protected-content-in-the-service-provider.md).

> [!Note]  
> la plupart des méthodes de transfert de fichiers ou de demandes de transfert de fichiers Gestionnaire de périphériques Windows échouent (souvent avec une valeur de **HRESULT** mystérieuse) lors de la gestion des fichiers protégés par DRM avec un débogueur attaché. par conséquent, vous devez utiliser d’autres méthodes pour déboguer votre code, telles que la journalisation des sorties dans un formulaire de Windows ou un fichier journal. Pour plus d’informations sur les options de journalisation, consultez Activation de la [journalisation](enabling-logging.md). Si vous exécutez un débogueur sur du contenu protégé, une méthode retourne l’un des codes d’erreur répertoriés dans les [codes d’erreur](error-codes.md)de la section DRM, ou éventuellement un code d’erreur inconnu. Si vous recevez des valeurs de **HRESULT** mystérieuses lors de l’exécution d’un débogueur sur du contenu ou des méthodes protégés, la protection DRM peut en être la cause.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




