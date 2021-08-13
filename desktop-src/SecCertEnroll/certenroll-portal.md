---
description: Exemple de certificat. Créer des applications pour la certification d’API, installer un certificat SSL, un certificat de serveur, créer un certificat sur un support, tel qu’Internet ou un intranet, qui ne sont pas sécurisés par nature.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API d’inscription de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df9caf38f22ac2c8ca8b13e6ca471eea94ae10b5c01ee2da7b4c2247844a70c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902959"
---
# <a name="certificate-enrollment-api"></a>API d’inscription de certificats

## <a name="purpose"></a>Objectif

L’API d’inscription de certificats peut être utilisée pour créer une application cliente afin de demander un certificat et d’installer une réponse de certificat. cette API est implémentée dans CertEnroll.dll à partir de Windows Vista ; Il remplace Xenroll.dll.

## <a name="developer-audience"></a>Développeurs concernés

L’API d’inscription de certificats est destinée aux développeurs d’applications qui permettent aux utilisateurs de créer, de demander et de récupérer des certificats sur des médias, tels qu’Internet ou un intranet, qui ne sont pas sécurisés par nature. les développeurs doivent être familiarisés avec les langages de programmation C et C++, le modèle COM (Component Object Model) et l’environnement de programmation basé sur les Windows. Bien que cela ne soit pas obligatoire, il est recommandé de comprendre le chiffrement et l’infrastructure de clé publique.

## <a name="run-time-requirements"></a>Conditions d’exécution

l’API d’inscription de certificats est prise en charge à partir de Windows Server 2008 et Windows Vista. Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de l’API d’inscription de certificats](about-the-certificate-enrollment-api.md)<br/> | Les concepts clés relatifs aux demandes de certificat sont décrits.<br/>                                                                                                      |
| [Utilisation de l’API d’inscription de certificats](using-the-certificate-enrollment-api.md)<br/> | Comment utiliser l’API d’inscription de certificats pour étendre les fonctionnalités de Active Directory les services de certificats.<br/>                                              |
| [Référence de l’API d’inscription de certificats](certificate-enrollment-api-reference.md)<br/> | Description détaillée des interfaces, énumérations et autres éléments de programmation qui peuvent être utilisés pour inscrire un utilisateur ou un ordinateur dans une hiérarchie de certificats.<br/> |



 

 

 




