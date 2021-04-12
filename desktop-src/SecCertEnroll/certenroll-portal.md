---
description: Exemple de certificat. Créer des applications pour la certification d’API, installer un certificat SSL, un certificat de serveur, créer un certificat sur un support, tel qu’Internet ou un intranet, qui ne sont pas sécurisés par nature.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API d’inscription de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526337"
---
# <a name="certificate-enrollment-api"></a>API d’inscription de certificats

## <a name="purpose"></a>Objectif

L’API d’inscription de certificats peut être utilisée pour créer une application cliente afin de demander un certificat et d’installer une réponse de certificat. Cette API est implémentée dans CertEnroll.dll à partir de Windows Vista. Il remplace Xenroll.dll.

## <a name="developer-audience"></a>Développeurs concernés

L’API d’inscription de certificats est destinée aux développeurs d’applications qui permettent aux utilisateurs de créer, de demander et de récupérer des certificats sur des médias, tels qu’Internet ou un intranet, qui ne sont pas sécurisés par nature. Les développeurs doivent être familiarisés avec les langages de programmation C et C++, le modèle COM (Component Object Model) et l’environnement de programmation Windows. Bien que cela ne soit pas obligatoire, il est recommandé de comprendre le chiffrement et l’infrastructure de clé publique.

## <a name="run-time-requirements"></a>Conditions d’exécution

L’API d’inscription de certificats est prise en charge à partir de Windows Server 2008 et Windows Vista. Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de l’API d’inscription de certificats](about-the-certificate-enrollment-api.md)<br/> | Les concepts clés relatifs aux demandes de certificat sont décrits.<br/>                                                                                                      |
| [Utilisation de l’API d’inscription de certificats](using-the-certificate-enrollment-api.md)<br/> | Comment utiliser l’API d’inscription de certificats pour étendre les fonctionnalités de Active Directory les services de certificats.<br/>                                              |
| [Référence de l’API d’inscription de certificats](certificate-enrollment-api-reference.md)<br/> | Description détaillée des interfaces, énumérations et autres éléments de programmation qui peuvent être utilisés pour inscrire un utilisateur ou un ordinateur dans une hiérarchie de certificats.<br/> |



 

 

 




