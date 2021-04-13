---
title: Gestion du contenu protégé
description: Gestion du contenu protégé
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Gestionnaire de périphériques Windows Media, certificats
- Gestionnaire de périphériques, certificats
- applications de bureau, certificats
- fournisseurs de services, certificats
- Guide de programmation, certificats
- certificates
- Gestionnaire de périphériques Windows Media, fournisseur de contenu sécurisé (SCP)
- Gestionnaire de périphériques, fournisseur de contenu sécurisé (SCP)
- applications de bureau, fournisseur de contenu sécurisé (SCP)
- fournisseurs de services, fournisseur de contenu sécurisé (SCP)
- Guide de programmation, fournisseur de contenu sécurisé (SCP)
- fournisseur de contenu sécurisé (SCP)
- SCP (Secure Content Provider)
- Gestionnaire de périphériques Windows Media, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Guide de programmation, contenu protégé par DRM
- applications de bureau, contenu protégé par DRM
- fournisseurs de services, contenu protégé par DRM
- Contenu protégé par DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379801"
---
# <a name="handling-protected-content"></a>Gestion du contenu protégé

Si vous créez une application ou un fournisseur de services qui consomme du contenu protégé par la gestion des droits numériques (DRM) Windows Media, vous devez disposer d’une paire clé/certificat émise par Microsoft. Pour savoir où obtenir ce certificat, consultez [outils de développement](tools-for-development.md). Si vous n’envisagez pas de gérer le contenu protégé, vous pouvez utiliser la clé factice et le certificat fournis avec ce kit de développement logiciel (SDK) dans un fichier nommé Key. c.

Pour tout fichier protégé par la technologie DRM, Windows Media Gestionnaire de périphériques nécessite la présence d’un fournisseur de contenu sécurisé (SCP) pour ce format de fichier. Microsoft fournit un module SCP pour les fichiers WMA et WMV. Si votre application ou fournisseur de services gère le contenu DRM protégé d’un autre format, vous devez fournir votre propre module SCP. Un module SCP est un objet COM qui implémente toutes les [interfaces des fournisseurs de contenu sécurisés](interfaces-for-secure-content-providers.md).

Une application peut envoyer du contenu protégé par DRM à des appareils basés sur Windows Media DRM 10 pour les périphériques portables ou sur des DRM d’appareils mobiles (PDDRM). Toutefois, vous pouvez uniquement créer un fournisseur de services pour les appareils basés sur PDDRM ; vous ne pouvez pas créer un fournisseur de services pour les appareils basés sur Windows Media DRM 10 pour les appareils mobiles. Ces derniers appareils peuvent uniquement utiliser le fournisseur de services MTP fourni par Microsoft.

Les appareils basés sur PDDRM peuvent uniquement prendre en charge les licences pour le contenu acheté. Les licences qui ont des conditions d’expiration de délai sont uniquement prises en charge par les appareils basés sur Windows Media DRM 10 pour les appareils mobiles, qui ont des exigences particulières, telles que l’horloge sécurisée et l’individualisation. Le kit de développement logiciel (SDK) Windows Media DRM 10 pour appareils mobiles fournit des détails sur la configuration requise des appareils pour prendre en charge la technologie version 10.

Avant d’envoyer du contenu DRM à l’appareil, une application doit vérifier plusieurs éléments :

-   Que l’appareil prend en charge la technologie DRM.
-   La version de la technologie DRM prise en charge (version 10 ou antérieure).
-   Si l’appareil est basé sur la version 10, tous ses composants sont à jour (par exemple, l’horloge sécurisée et toutes les exigences d’individualisation).

Tous les appels de méthode pour répondre à ces questions sont faits par le client et gérés par les Gestionnaire de périphériques Windows Media et le composant fournisseur de contenu sécurisé. le fournisseur de services ne gère aucun de ces appels.

Si l’appareil ne prend pas en charge Windows Media DRM 10 pour les appareils mobiles, il peut toujours être en mesure de consommer du contenu protégé (en fonction de la licence de contenu et de la conception de l’appareil), mais tout contenu qui lui est envoyé disposera d’une licence d’utilisation simplifiée avec des droits limités (par exemple, pas de délai d’expiration).

-   Pour obtenir des exemples montrant comment une application vérifie si un appareil peut gérer du contenu protégé et s’il doit mettre à jour ses composants DRM, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md).
-   Pour plus d’informations sur la création d’un fournisseur de services pouvant gérer du contenu protégé, consultez [gestion du contenu protégé dans le fournisseur de services](handling-protected-content-in-the-service-provider.md).

> [!Note]  
> Un grand nombre de méthodes de transfert de fichiers ou de droits Windows Media Gestionnaire de périphériques échouent (souvent avec une valeur de **HRESULT** mystérieuse) lors de la gestion des fichiers protégés par DRM avec un débogueur attaché. Par conséquent, vous devez utiliser d’autres méthodes pour déboguer votre code, telles que la journalisation des sorties dans un Windows Form ou un fichier journal. Pour plus d’informations sur les options de journalisation, consultez Activation de la [journalisation](enabling-logging.md). Si vous exécutez un débogueur sur du contenu protégé, une méthode retourne l’un des codes d’erreur répertoriés dans les [codes d’erreur](error-codes.md)de la section DRM, ou éventuellement un code d’erreur inconnu. Si vous recevez des valeurs de **HRESULT** mystérieuses lors de l’exécution d’un débogueur sur du contenu ou des méthodes protégés, la protection DRM peut en être la cause.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




