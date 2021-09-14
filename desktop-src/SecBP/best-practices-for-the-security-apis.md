---
description: Suggestions pour les évaluations de la sécurité des applications pour le développement d’applications de logiciels de sécurité Windows et le développement de logiciels sécurisés, y compris les tests de sécurité des applications.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Meilleures pratiques pour les API de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa821cfbaa9874d17559ad0e81f636fbaddd14f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011189"
---
# <a name="best-practices-for-the-security-apis"></a>Meilleures pratiques pour les API de sécurité

Pour faciliter le développement de logiciels sécurisés, nous vous recommandons d’utiliser les meilleures pratiques suivantes lors du développement d’applications. Pour plus d’informations, consultez [Security Developer Center](https://msdn.microsoft.com/security/default.aspx).

## <a name="security-development-life-cycle"></a>Cycle de vie du développement de sécurité

Le [cycle de vie de développement](/previous-versions/ms995349(v=msdn.10)) de la sécurité (SDL) est un processus qui aligne une série d’activités et de livrables axées sur la sécurité pour chaque phase du développement logiciel. Ces activités et ces livrables sont les suivants :

-   Développement de modèles de menaces
-   Utilisation d’outils d’analyse de code
-   Révisions du code et test de sécurité

Pour plus d’informations sur le SDL, consultez le [blog SDL](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Modèles de menace

La réalisation d’une analyse du modèle des menaces peut vous aider à découvrir les points d’attaque potentiels dans votre code. Pour plus d’informations sur l’analyse du modèle des menaces, consultez Howard, Michael et LeBlanc, David \[ 2003 \] , *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. (Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)

## <a name="service-packs-and-security-updates"></a>Service Packs et mises à jour de sécurité

Les environnements de génération et de test doivent refléter les mêmes niveaux de service packs et les mises à jour de sécurité de la base d’utilisateurs ciblée. Nous vous recommandons d’installer les service packs et les mises à jour de sécurité les plus récents pour toute plateforme ou application Microsoft qui fait partie de votre environnement de création et de test et encourager les utilisateurs à faire de même pour l’environnement d’application final. pour plus d’informations sur les service packs et les mises à jour de sécurité, consultez [microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) et [sécurité microsoft](https://www.microsoft.com/security).

## <a name="authorization"></a>Autorisation

Vous devez créer des applications qui nécessitent le moins de privilèges possible. L’utilisation du moindre privilège possible réduit le risque de compromission du code malveillant par le système informatique. Pour plus d’informations sur l’exécution du code au moins de niveau de privilège possible, consultez [exécution avec des privilèges spéciaux](running-with-special-privileges.md).

## <a name="more-information"></a>Informations complémentaires

Pour plus d’informations sur les meilleures pratiques, consultez les rubriques suivantes.



| Rubrique                                                                                                                        | Description                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Exécution avec des privilèges spéciaux](running-with-special-privileges.md)<br/>                                            | Décrit les implications de la sécurité des privilèges.<br/>                                                                                                                                  |
| [Éviter les dépassements de mémoire tampon](avoiding-buffer-overruns.md)<br/>                                                          | Fournit des informations sur l’évitement des dépassements de mémoire tampon.<br/>                                                                                                                            |
| [Control Flow Guard (CFG) ](control-flow-guard.md)<br/>                                                                | Décrit les vulnérabilités d’altération de la mémoire.<br/>                                                                                                                                    |
| [Création d’une liste DACL](creating-a-dacl.md)<br/>                                                                            | Montre comment créer une liste de contrôle d’accès discrétionnaire (DACL) à l’aide du langage SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ).<br/> |
| [Gestion des mots de passe](handling-passwords.md)<br/>                                                                      | Décrit les implications en matière de sécurité lors de l’utilisation de mots de passe.<br/>                                                                                                                             |
| [Comment optimiser votre recherche dans la bibliothèque MSDN](how-to-optimize-your-msdn-library-search.md)<br/>                          | Décrit les options de recherche de contenu du SDK de sécurité sur MSDN Library.<br/>                                                                                                           |
| [Extensibilité du développeur de Access Control dynamique](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Orientation de base pour certains points d’extensibilité de développeur pour les nouvelles solutions de Access Control dynamique.<br/>                                                                   |



 

 

