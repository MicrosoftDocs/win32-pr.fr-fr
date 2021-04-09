---
title: Appel des dll d’extension
description: Appelle ces fonctions pour chaque paquet d’authentification ou de gestion des comptes valide qu’il reçoit du serveur d’accès au réseau (NAS).
ms.assetid: 6d738ad7-cce5-4835-97d6-c57173c79a16
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc96fab078a982f23f5f5dd86d51dbed46d5541
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941220"
---
# <a name="invoking-the-extension-dlls"></a>Appel des dll d’extension

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Les dll d’extension NPS doivent exporter au moins l’une des fonctions de rappel suivantes : [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process), [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)ou [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2). NPS appelle ces fonctions pour chaque paquet d’authentification ou de gestion des comptes valide qu’il reçoit du serveur d’accès au réseau (NAS). Le serveur NPS appelle ces fonctions dans chacune des dll listées sous la [clé de registre des paramètres](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)du serveur NPS. Les dll sont appelées dans l’ordre dans lequel elles sont répertoriées.

Si une DLL d’extension NPS exporte plusieurs des fonctions ci-dessus, le serveur NPS appelle simplement l’une d’entre elles : la fonction la plus récente prise en charge par le système d’exploitation.

> [!Note]  
> IAS a initialement pris en charge uniquement [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process). IAS prend également en charge [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex). IAS (et les versions ultérieures de NPS) prend également en charge [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2).

 

Les dll d’extension NPS peuvent également exporter les fonctions [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) et [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) . S’ils sont présents, le serveur NPS appelle ces fonctions lorsque le service démarre et s’arrête, respectivement.

## <a name="radiusextensionprocess-callback-function"></a>RadiusExtensionProcess fonction de rappel

Dans une DLL d’extension d’authentification, [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) reçoit tous les attributs qui sont reçus par NPS dans la demande d’authentification ou de gestion des comptes. À l’aide de ces attributs, la fonction peut effectuer des validations supplémentaires, vérifier les autorisations de l’utilisateur ou envoyer des enregistrements de gestion de comptes à un serveur d’État central.

Dans une DLL d’extension d’autorisation, **RadiusExtensionProcess** reçoit tous les attributs générés par le service d’autorisation NPS. Il s’agit des attributs qui sont retournés dans le paquet Access-Accept.

Après l’appel de **RadiusExtensionProcess**, l’action effectuée par le serveur NPS dépend de la valeur de retour de **RadiusExtensionProcess** et de la valeur retournée dans le paramètre *pfAction* . Ces valeurs sont répertoriées dans le tableau suivant.



| *pfAction* | DLL d’extension d’authentification                                                                                                                                            | DLL d’extension d’autorisation                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accepter     | Ignore les autres DLL d’extension d’authentification et contourne également le mécanisme d’authentification NPS.                                                                  | Accepter non autorisé.                                                                                                                                         |
| Rejeter     | Ignore les autres DLL d’extension d’authentification et contourne également le mécanisme d’authentification NPS. Access-Reject paquet est envoyé.                                    | Ignore toutes les autres DLL d’extension d’autorisation.                                                                                                          |
| Continuer   | Le paquet est envoyé à la prochaine DLL d’extension d’authentification ou au mécanisme d’authentification NPS si aucune autre DLL d’extension d’authentification n’est répertoriée dans le registre. | Le paquet est envoyé à la DLL d’extension d’autorisation suivante ou au Journal de gestion des comptes NPS si aucune autre DLL d’extension d’autorisation n’est répertoriée dans le registre. |



 

Pour toutes les dll d’extension, si **RadiusExtensionProcess** retourne une erreur, le paquet est ignoré. Les paquets ignorés en raison d’une erreur ne sont pas traités par le journal de gestion des comptes NPS.

Si une erreur se produit, NPS publie un événement d’erreur générique dans le journal des événements. Il est recommandé que la DLL d’extension fournisse une journalisation des erreurs supplémentaire.

Pour plus d’informations et pour obtenir un diagramme qui représente le processus précédent, consultez [à propos des extensions NPS](/windows/desktop/Nps/ias-about-internet-authentication-service).

**RadiusExtensionProcess** doit retourner une erreur s’il ne peut pas vérifier l’acceptation ou le rejet du paquet. Cette situation peut se produire si un problème réseau empêche **RadiusExtensionProcess** de communiquer avec sa base de données d’authentification utilisateur.

Lors du traitement d’un paquet de comptabilité, le paramètre *pfAction* est **null**, donc *pfAction* ne peut pas être défini. Le renvoi d’une erreur à partir de la fonction **RadiusExtensionProcess** lors du traitement d’une demande de gestion entraîne la suppression de la demande par le serveur NPS.

> [!Note]  
> Après avoir reçu une acceptation, NPS n’appelle pas **RadiusExtensionProcess** dans les autres dll de la séquence. Étant donné que certaines fonctions d’authentification peuvent également implémenter des autorisations, les fonctions d’authentification ignorées peuvent entraîner l’omission des autorisations. Si une instance de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) retourne Accept, il est important de ne pas faire d’hypothèses sur les autorisations récupérées.

 

Si la valeur continue ou Accept est retournée, le profil correspondant au domaine est renvoyé dans le paquet Access-Accept.

Les dll d’extension d’authentification doivent être conçues pour coexister avec les fournisseurs d’authentification NPS intégrés et avec d’autres DLL d’extension. Si une extension s’applique uniquement à une certaine base de données utilisateur (par exemple, Windows Active Directory), elle doit vérifier l’attribut [**ratProvider**](/windows/desktop/api/authif/ne-authif-radius_authentication_provider) transmis dans *le paramètre des* modèles, avant de traiter la demande. L’attribut ratProvider serait une liste d’attributs vers laquelle pointe *le paramètre de* modèles.

Les dll d’extension ne doivent pas rejeter les demandes, car les attributs requis sont manquants. Par exemple, si une extension d’authentification requiert l’attribut User-Password, ratUserPassword et que l’attribut n’est pas présent, l’extension doit retourner une action de raContinue pour permettre à d’autres extensions et fournisseurs de traiter la demande.

Le serveur NPS appelle la fonction [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) après avoir décidé d’utiliser une base de données d’authentification particulière, mais avant que l’utilisateur soit authentifié. Par conséquent, les informations relatives à la base de données d’authentification à utiliser sont disponibles pour la fonction, afin que la fonction puisse vérifier les autorisations de l’utilisateur dans la base de données d’authentification appropriée. NPS prend en charge différentes bases de données d’authentification, y compris Windows Active Directory.

## <a name="radiusextensionprocessex-callback-function"></a>RadiusExtensionProcessEx fonction de rappel

Les dll d’extension NPS peuvent exporter des [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) au lieu de ou en plus de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process). Cette fonction permet à la DLL d’ajouter des attributs d’autorisation supplémentaires à la réponse d’authentification.

Les informations décrites dans la section *fonction de rappel RadiusExtensionProcess* s’appliquent à la fonction [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) .

[**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) ne peut pas modifier ou supprimer les attributs présents. Si un scénario se produit dans lequel la DLL doit modifier ou supprimer des attributs, la seule option consiste à utiliser l’interface utilisateur du serveur NPS pour s’assurer que les attributs ne sont pas présents. Par défaut, aucun attribut d’autorisation n’est présent. Tous ceux qui sont présents doivent avoir été ajoutés par le biais de l’interface utilisateur.

Si plusieurs DLL d’autorisation sont configurées et que certaines de ces dll implémentent [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), la fonction **RadiusExtensionProcess/ex** dans une dll donnée ne reçoit pas les attributs des dll d’autorisation précédemment appelées. Il reçoit uniquement les attributs générés par le service d’autorisation NPS.

## <a name="radiusextensionprocess2-callback-function"></a>RadiusExtensionProcess2 fonction de rappel

Les dll d’extension NPS peuvent également exporter des [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) au lieu de, ou en plus de, [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) et **RadiusExtensionProcessEx**. Cette fonction permet à la DLL d’ajouter, de modifier et de supprimer des attributs vers et à partir de la demande ou de la réponse d’authentification.

Les informations décrites dans la section *fonction de rappel RadiusExtensionProcessEx* s’appliquent à la fonction [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) , avec les exceptions suivantes :

-   Dans une DLL d’autorisation, **RadiusExtensionProcess2** reçoit à la fois les attributs générés par le service d’autorisation NPS et les attributs générés à partir des dll d’autorisation précédemment appelées.
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) n’a pas de paramètre *pfAction* . **RadiusExtensionProcess2** définit la disposition finale de la demande à l’aide de la fonction [**SetResponseType**](/previous-versions/ms688462(v=vs.85)) fournie dans la structure de [**bloc de \_ \_ contrôle \_ d’extension RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .
-   NPS appelle toujours la fonction [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) dans toutes les dll restantes, que les fonctions des dll précédentes aient retourné Accept.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration des dll d’extension](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Attributs d’identification utilisateur](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 