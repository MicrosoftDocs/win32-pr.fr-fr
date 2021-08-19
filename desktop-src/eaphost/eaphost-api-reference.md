---
title: Informations de référence sur l’API EAPHost
description: En savoir plus sur les API EAPHost et leurs composants. Consultez les informations de référence pour les différentes rubriques d’API, comme le schéma XML EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c522698999bcb58b4e33b8e1cb0d1bb74ae64fc3b709ce672b35e7db81e85ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739099"
---
# <a name="eaphost-api-reference"></a>Informations de référence sur l’API EAPHost

Les API EAPHost sont divisées en trois composants : les API du demandeur, qui peuvent être directement appelées à partir d’une application compatible EAP. les API de méthode d’homologue EAP, qui gèrent les demandes des demandeurs pour un type d’authentification EAP spécifique et déclenchent des éléments interactifs sur le client ; et les API de l’authentificateur EAP, qui effectuent l’authentification côté serveur d’un demandeur.

les deux derniers composants d’api : la méthode d’homologue eap et les api de méthode d’Authenticator eap--nécessitent une implémentation personnalisée et conforme dans des dll qui les exposent au service EAPHost. Elles ne peuvent pas être appelées directement à partir du code d’application ; au lieu de cela, elles sont appelées par EAPHost (côté client pour les méthodes homologues EAP et côté serveur pour les méthodes d’authentificateur EAP) si l’implémentation correspond aux signatures d’API spécifiées dans la documentation correspondante. Les informations spécifiques à l’implémentation de l’API sont fournies sur chaque page de référence de fonction.

## <a name="eaphost-registry-settings"></a>Paramètres du registre EAPHost



| Rubrique                                                      | Description                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [Paramètres du registre EAPHost](eaphost-registry-settings.md) | Décrit les clés de Registre consommées par EAPHost. |



 

## <a name="eaphost-xml-schema"></a>Schéma XML EAPHost



| Rubrique                                            | Description                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost et schéma hérité](eaphost-schemas.md) | Décrit le schéma EAPHost et le schéma hérité pour créer des données XML de configuration et des informations d’identification XML. |



 

## <a name="common-eaphost-api-reference"></a>Informations de référence sur les API EAPHost courantes



| Rubrique                                                                   | Description                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Énumérations d’API EAPHost courantes](common-eap-host-api-enumerations.md) | Répertorie les constantes communes à toutes les API EAPHost.  |
| [Structures d’API EAPHost courantes](common-eap-host-api-structures.md)     | Répertorie les structures communes à toutes les API EAPHost. |
| [Constantes d’API EAPHost courantes](common-eap-host-error-constants.md)     | Répertorie les constantes communes à toutes les API EAPHost.  |



 

## <a name="eaphost-api-reference"></a>Informations de référence sur l’API EAPHost



| Rubrique                                                                       | Description                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informations de référence sur l’API Supplier EAPHost](eap-host-supplicant-api-reference.md)   | Décrit les éléments d’API disponibles pour activer les appels de demandeur à EAPHost.                                                                      |
| [Informations de référence sur l’API de méthode homologue EAPHost](eap-host-peer-method-api-reference.md) | Décrit les éléments d’API qui doivent être implémentés pour créer une DLL de méthode homologue EAP qui peut être chargée et appelée par une EAPHost cliente.          |
| [api de méthode Authenticator EAPHost](eaphost-authenticator-method-apis.md)  | Décrit les éléments d’API qui doivent être implémentés pour créer une DLL de méthode d’authentificateur EAP qui peut être chargée et appelée par un serveur EAPHost. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos d’EAPHost](about-eap-host.md)
</dt> <dt>

[Utilisation d’EAPHost](using-eap-host.md)
</dt> </dl>

 

 




