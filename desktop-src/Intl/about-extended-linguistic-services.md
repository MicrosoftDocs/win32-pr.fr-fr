---
description: Les services linguistiques étendus (ELS) sont implémentés sous la forme d’une bibliothèque de liens dynamiques (DLL) qui fournit diverses fonctionnalités de prise en charge linguistique pour le texte que l’application spécifie.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: À propos des services linguistiques étendus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240497"
---
# <a name="about-extended-linguistic-services"></a>À propos des services linguistiques étendus

Les services linguistiques étendus (ELS) sont implémentés sous la forme d’une bibliothèque de liens dynamiques (DLL) qui fournit diverses fonctionnalités de prise en charge linguistique pour le texte que l’application spécifie. La technologie comprend la plateforme et les plug-ins ELS pour plusieurs types de service linguistiques prédéfinis accessibles à l’application via la plateforme.

> [!Note]  
> le module ELS est installé automatiquement avec Windows 7 et versions ultérieures.

 

## <a name="els-platform"></a>Plateforme ELS

La plateforme ELS est l’interface entre votre application et les services ELS. Il offre un moyen simple d’implémenter plusieurs types de fonctionnalités linguistiques via la même API, ce qui permet à l’application d’accéder à des services spécifiques et de les utiliser. Pour plus d’informations sur l’API, consultez [référence des services linguistiques étendus.](extended-linguistic-services-reference.md)

> [!Note]  
> Lorsque l’application appelle l’une des fonctions de l’API ELS, la plateforme alloue la mémoire et les ressources nécessaires pour la communication avec les services. L’application est responsable de l’appel de la plateforme pour libérer ces ressources.

 

La plateforme s’exécute dans l’espace mémoire virtuelle de l’application, et toute la mémoire allouée fait partie de cet espace. Par conséquent, votre application doit uniquement être liée à la DLL du composant ELS (Elscore.dll) en établissant une liaison à Elscore. lib ou en chargeant dynamiquement Elscore.dll.

## <a name="els-services"></a>Services ELS

pour les Windows 7 et versions ultérieures, la plateforme ELS prend en charge uniquement les services prédéfinis suivants.

-   [Détection de langue Microsoft](microsoft-language-detection.md)
-   [Détection de scripts Microsoft](microsoft-script-detection.md)
-   [Services de translittération](transliteration-services.md)

> [!Note]  
> Les futures versions d’ELS prendront en charge des services supplémentaires fournis par Microsoft ou des fournisseurs de services.

 

Chaque service est associé à une catégorie de service décrivant ce que fait le service. La catégorie est représentée par une chaîne non localisable. Elle est utilisée par les applications pour énumérer les services disponibles. Les catégories de service actuelles sont les suivantes :

-   « Détection de langue »
-   « Détection de script »
-   Translittér

La plateforme utilise des métadonnées de service pour énumérer les services demandés par l’application. Les propriétés telles que l’identificateur global unique (GUID) du service, les langues et les scripts d’entrée et de sortie pris en charge et la catégorie de service peuvent être utilisées par l’application pour énumérer les services ELS souhaités.

Chaque service ELS est implémenté en tant que plug-in pris en charge par une DLL qui peut être installée sur le système d’exploitation afin que la plateforme ELS puisse le détecter et l’utiliser. Les services peuvent exposer leurs propres sous-services, si nécessaire.

## <a name="main-els-operations"></a>Opérations ELS principales

Cette section décrit les principales opérations prises en charge par la plateforme ELS. La plateforme prend en charge les modes d’appel synchrones et asynchrones. Le mode d’appel asynchrone utilise un pool de threads d’application pour planifier les threads de traitement des demandes.

> [!Note]  
> Étant donné que la plateforme prend en charge un mode asynchrone, les services ELS n’ont pas à implémenter ce type de fonctionnalité de manière autonome.

 

### <a name="service-enumeration"></a>Énumération de service

La plateforme ELS charge et gère tous les services ELS, ce qui rend l’opération transparente pour l’application. L’application énumère les services disponibles en appelant [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices). Pour obtenir des instructions de programmation, consultez [énumération et libération de services](enumerating-and-freeing-services.md).

> [!Note]  
> Pour des raisons de performances, il est recommandé de faire en sorte que votre application n’énumère les services disponibles qu’une seule fois. La plateforme ELS vérifie à nouveau les services sur l’énumération suivante pour s’assurer que les résultats de leur énumération sont toujours à jour.

 

### <a name="text-recognition"></a>Reconnaissance de texte

Après l’énumération de service, l’application appelle la fonction [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) pour utiliser un service Els particulier afin de mapper une plage de texte de texte d’entrée au texte de sortie. Un exemple de reconnaissance de texte est l’utilisation d’un service de détection de langage qui reçoit un segment de texte et détecte son langage le plus probable.

Une fois que le service a reconnu le texte, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retourne avec une structure de [**\_ \_ jeu**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) de propriétés de mappage remplie avec les données de sortie et les propriétés produites par le service. Pour éviter les fuites de mémoire, l’application doit libérer le conteneur de propriétés en appelant [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) pour chaque fois que le [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retourne S \_ OK. En règle générale, l’application effectue cette opération lorsqu’elle a terminé d’utiliser les données de sortie ou lorsque les données de sortie ne sont plus pertinentes, car la région d’entrée du texte a été modifiée, par exemple, modifiée ou supprimée. Lorsque le jeu de propriétés est relâché, **MappingFreePropertyBag** retourne.

Des instructions de programmation pour la reconnaissance de texte sont fournies dans [demande de reconnaissance de texte](requesting-text-recognition.md).

### <a name="service-termination"></a>Arrêt du service

Lorsque votre application n’a plus besoin de services ELS, elle appelle [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) avant qu’elle ne se termine. Pour plus d’informations, consultez [énumération et libération de services](enumerating-and-freeing-services.md).

### <a name="versioning"></a>Contrôle de version

Les futures versions d’ELS autorisent la mise à jour des services ELS. L’application sera en mesure de vérifier les numéros de version de la structure d' [**\_ \_ informations de service de mappage**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) pour détecter les modifications apportées aux services.

> [!Note]  
> Votre application ELS ne doit pas supposer que les différentes versions du même service peuvent récupérer exactement les mêmes résultats.

 

 

 



