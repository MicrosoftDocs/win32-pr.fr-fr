---
title: Utilisation de DsAddSidHistory
description: Cette rubrique explique comment utiliser la fonction DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Utilisation de DsAddSidHistory Active Directory
- Active Directory Active Directory, utilisation de, à l’aide de DsAddSidHistory
- DsAddSidHistory Active Directory, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796bd2bfb46ac8323a4fac7e9b6498a63faf58c8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465616"
---
# <a name="using-dsaddsidhistory"></a>Utilisation de DsAddSidHistory

La fonction [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) obtient l’identificateur de sécurité (SID) du compte principal d’un principal de sécurité d’un domaine (le domaine source) et l’ajoute à l’attribut **SIDHistory** d’un principal de sécurité dans un autre domaine (de destination) d’une autre forêt. lorsque le domaine source est en mode natif Windows 2000, cette fonction récupère également les valeurs **sIDHistory** du principal source et les ajoute au **sidhistory** du principal de destination.

L’ajout de sid au **SIDHistory** d’un principal de sécurité est une opération sensible à la sécurité qui accorde efficacement au principal de destination l’accès à toutes les ressources accessibles au principal source, à condition que des approbations existent entre les domaines de ressources applicables et le domaine de destination.

dans un domaine Windows 2000 en mode natif, une ouverture de session utilisateur crée un jeton d’accès qui contient le sid du compte principal de l’utilisateur et les sid de groupe, ainsi que le **sidhistory** de l’utilisateur et le **sidhistory** des groupes dont l’utilisateur est membre. Le fait d’avoir ces anciens sid (valeurs **SIDHistory** ) dans le jeton de l’utilisateur accorde à l’utilisateur l’accès aux ressources protégées par des listes de contrôle d’accès (ACL) contenant les anciens sid.

cette opération facilite certains scénarios de déploiement Windows 2000. en particulier, il prend en charge un scénario dans lequel les comptes d’une nouvelle forêt Windows 2000 sont créés pour les utilisateurs et les groupes qui existent déjà dans un environnement de production Windows NT 4,0. en plaçant le SID de compte Windows NT 4,0 dans le compte Windows **2000, l'** accès aux ressources réseau est préservé pour que l’utilisateur se connecte à son nouveau compte Windows 2000.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) prend également en charge la migration des serveurs de ressources des contrôleurs de domaine de sauvegarde Windows NT 4,0 (ou des contrôleurs de domaine et des serveurs membres en mode natif Windows domaine 2000) vers un domaine Windows 2000 en tant que serveurs membres. pour cette migration, vous devez créer, dans le domaine de destination Windows 2000, les groupes locaux de domaine qui contiennent, dans leur **sIDHistory**, les sid principaux des groupes locaux définis sur le BDC (ou les groupes locaux de domaine référencés dans les listes de contrôle d’accès sur les serveurs Windows 2000) dans le domaine source. En créant un groupe local de destination contenant le **SIDHistory** et tous les membres du groupe local source, l’accès aux ressources serveur migrées, protégées par des ACL référençant le groupe local source, est conservé pour tous les membres.

> [!Note]  
> L’utilisation de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) nécessite une compréhension des implications administratives et de sécurité plus larges dans ces scénarios et dans d’autres scénarios. pour plus d’informations, consultez le livre blanc « planification de la Migration de Windows NT vers Microsoft Windows 2000 », fourni comme Dommig.doc dans les outils de Support Windows 2000. Cette documentation est également disponible sur le CD du produit \\ , sous \\ outils de support.

 

## <a name="authorization-requirements"></a>Conditions d’autorisation

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiert des privilèges d’administrateur dans les domaines source et de destination. Plus précisément, l’appelant de cette API doit être membre du groupe administrateurs de domaine dans le domaine de destination. Une vérification codée en dur pour cette appartenance est effectuée. En outre, l’appelant ou le compte fourni dans le paramètre *SrcDomainCreds* , s’il n’est pas **null**, doit être membre du groupe administrateurs ou administrateurs de domaine dans le domaine source.

## <a name="domain-and-trust-requirements"></a>Exigences relatives au domaine et à la confiance

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiert que le domaine de destination soit en mode natif Windows 2000 ou ultérieur, car seul ce type de domaine prend en charge l’attribut **sIDHistory** . le domaine source peut être Windows NT 4,0 ou Windows 2000, en mode mixte ou natif. Les domaines source et de destination ne doivent pas se trouver dans la même forêt. Windows Les domaines NT 4,0 sont par définition non dans une forêt. Cette contrainte inter-forêts garantit que les SID dupliqués, qu’ils apparaissent en tant que sid primaires ou valeurs **SIDHistory** , ne sont pas créés dans la même forêt.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiert une approbation externe entre le domaine source et le domaine de destination dans les cas indiqués dans le tableau suivant.



| Cas                                                                             | Description                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| le domaine source est Windows 2000.<br/>                                    | l’attribut **sIDHistory** source, disponible uniquement dans les domaines sources Windows 2000, peut être en lecture seule à l’aide de LDAP, ce qui nécessite cette approbation pour la protection de l’intégrité.<br/>                                                                                             |
| Le domaine source est Windows NT 4,0 et *SrcDomainCreds* a la **valeur null**.<br/> | L’emprunt d’identité, requis pour prendre en charge les opérations de domaine source à l’aide des informations d’identification de l’appelant, dépend de cette approbation. L’emprunt d’identité requiert également que le contrôleur de domaine de destination ait la valeur « approuvé pour la délégation » activée par défaut sur les contrôleurs de domaine.<br/> |



 

Toutefois, aucune approbation n’est requise entre les domaines source et de destination si le domaine source est Windows NT 4,0 et *SrcDomainCreds* n’a pas la **valeur null**.

## <a name="source-domain-controller-requirements"></a>Configuration requise du contrôleur de domaine source

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiert que le contrôleur de domaine, sélectionné comme cible pour les opérations dans le domaine source, soit le contrôleur de domaine principal dans Windows domaines NT 4,0 ou le Emulator pdc dans Windows domaines 2000. L’audit du domaine source est généré par le biais d’opérations d’écriture. par conséquent, le contrôleur de domaine principal est requis dans Windows domaines source NT 4,0, et la restriction de contrôleur de domaine principal garantit que les audits **DsAddSidHistory** sont générés sur un seul ordinateur. Cela réduit le besoin d’examiner les journaux d’audit de tous les contrôleurs de service pour surveiller l’utilisation de cette opération.

> [!Note]  
> Dans Windows domaines source NT 4,0, le contrôleur de domaine principal (Target of Operations in the source Domain) doit exécuter Service Pack 4 (SP4) et versions ultérieures pour garantir une prise en charge d’audit correcte.

 

la valeur de registre suivante doit être créée en tant que \_ valeur REG DWORD et définie sur 1 sur le contrôleur de domaine source pour les Windows NT 4,0 et Windows 2000 sources de contrôleurs de domaine.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

La définition de cette valeur active les appels RPC sur le transport TCP. Cela est nécessaire car, par défaut, les interfaces SAMRPC sont accessibles à distance uniquement sur les canaux nommés. L’utilisation de canaux nommés aboutit à un système de gestion des informations d’identification adapté aux utilisateurs connectés de manière interactive à effectuer des appels en réseau, mais n’est pas flexible pour un processus système qui effectue des appels réseau avec les informations d’identification fournies par l’utilisateur. RPC sur TCP est plus adapté à cet effet. La définition de cette valeur ne diminue pas la sécurité du système. Si cette valeur est créée ou modifiée, le contrôleur de domaine source doit être redémarré pour que ce paramètre prenne effet.

Un nouveau groupe local, « <SrcDomainName> $ $ $ », doit être créé dans le domaine source à des fins d’audit.

## <a name="auditing"></a>Audit

Les opérations [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) sont auditées pour s’assurer que les administrateurs de domaine source et de destination sont en mesure de détecter le moment où cette fonction a été exécutée. L’audit est obligatoire dans les domaines source et de destination. **DsAddSidHistory** vérifie que le mode d’audit est activé dans chaque domaine et que l’audit de gestion des comptes des événements de réussite/échec est activé. Dans le domaine de destination, un événement d’audit « ajouter l’historique des SID » unique est généré pour chaque opération **DsAddSidHistory** réussie ou ayant échoué.

Les événements d’audit « ajouter un historique des SID » uniques ne sont pas disponibles sur les systèmes Windows NT 4,0. Pour générer des événements d’audit qui reflètent sans ambiguïté l’utilisation de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) sur le domaine source, il effectue des opérations sur un groupe spécial dont le nom est l’identificateur unique dans le journal d’audit. Un groupe local, « <SrcDomainName> $ $ $ », dont le nom est composé du nom NetBIOS du domaine source est ajouté avec trois signes dollar ($) (code ASCII = 0x24 et Unicode = U + 0024), doit être créé sur le contrôleur de domaine source avant d’appeler **DsAddSidHistory**. Chaque utilisateur source et groupe global qui est une cible de cette opération est ajouté à, puis supprimé de l’appartenance de ce groupe. Cela génère des événements ajouter un membre et supprimer un membre dans le domaine source, qui peuvent être analysés en recherchant des événements qui référencent le nom du groupe.

> [!Note]  
> les opérations [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) sur les groupes locaux dans une Windows NT 4,0 ou Windows domaine source en mode mixte 2000 ne peuvent pas être auditées, car les groupes locaux ne peuvent pas être membres d’un autre groupe local et ne peuvent donc pas être ajoutés au <SrcDomainName> groupe local "$ $ $" spécial. Ce manque d’audit ne présente pas de problème de sécurité au domaine source, car l’accès aux ressources du domaine source n’est pas affecté par cette opération. L’ajout du SID d’un groupe local source à un groupe local de destination n’accorde pas l’accès aux ressources sources, protégées par ce groupe local, à des utilisateurs supplémentaires. L’ajout de membres au groupe local de destination ne leur accorde pas l’accès aux ressources sources. Les membres ajoutés bénéficient d’un accès uniquement aux serveurs du domaine de destination qui ont été migrés à partir du domaine source, qui peut avoir des ressources protégées par le SID du groupe local source.

 

## <a name="data-transmission-security"></a>Sécurité de la transmission de données

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) applique les mesures de sécurité suivantes :

-   appelé à partir d’une station de travail Windows 2000, les informations d’identification de l’appelant sont utilisées pour l’authentification et la confidentialité-protéger l’appel RPC au contrôleur de domaine de destination. Si *SrcDomainCreds* n’a pas la **valeur null**, la station de travail et le DC de destination doivent prendre en charge le chiffrement 128 bits pour la confidentialité-protéger les informations d’identification. Si le chiffrement 128 bits n’est pas disponible et que *SrcDomainCreds* est fourni, l’appel doit être effectué sur le contrôleur de l’emplacement de destination.
-   Le contrôleur de domaine de destination communique avec le contrôleur de domaine source à l’aide de *SrcDomainCreds* ou des informations d’identification de l’appelant pour l’authentification mutuelle et l’intégrité. Protégez la lecture du SID de compte source (à l’aide d’une recherche Sam) et **SIDHistory** (à l’aide d’une lecture LDAP).

## <a name="threat-models"></a>Modèles de menace

Le tableau suivant répertorie les menaces potentielles associées à l’appel [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) et traite les mesures de sécurité pertinentes pour une menace particulière.




| Menace potentielle | Mesure de sécurité | 
|------------------|------------------|
| Attaque de l’intercepteur<br /> Un utilisateur non autorisé intercepte le <em>SID de recherche de l’appel de retour de l’objet source</em> , en remplaçant le SID de l’objet source par un SID arbitraire à insérer dans un sIDHistory de l’objet cible.<br /> | Le <em>SID de recherche de l’objet source</em> est un RPC authentifié, à l’aide des informations d’identification d’administrateur de l’appelant, avec la protection des messages d’intégrité du paquet. Cela garantit que l’appel de retour ne peut pas être modifié sans détection. Le contrôleur de domaine de destination crée un événement d’audit « ajouter l’historique des SID » unique qui reflète le SID ajouté à la valeur <strong>SIDHistory</strong>du compte de destination.<br /> | 
| Domaine source cheval de Troie<br /> Un utilisateur non autorisé crée un domaine source « cheval de Troie » sur un réseau privé qui a le même SID de domaine et certains des mêmes SID de compte que le domaine source légitime. L’utilisateur non autorisé tente ensuite d’exécuter <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> dans un domaine de destination pour obtenir le SID d’un compte source. Cela s’effectue sans avoir besoin des informations d’identification d’administrateur de domaine source réelles et sans laisser de piste d’audit dans le véritable domaine source. La méthode d’utilisateur non autorisée pour créer le domaine source cheval de Troie peut être l’une des suivantes :<ul><li>Obtenez une copie (sauvegarde BDC) du domaine source SAM.</li><li>Créez un nouveau domaine, en modifiant le SID du domaine sur le disque afin qu’il corresponde au SID du domaine source légitime, puis créez suffisamment d’utilisateurs pour instancier un compte avec le SID souhaité.</li><li>Créer un réplica BDC. Cela nécessite des informations d’identification d’administrateur de domaine source. L’utilisateur non autorisé utilise ensuite le réplica sur un réseau privé pour mettre en œuvre l’attaque.</li></ul><br /> | Bien qu’il existe de nombreuses façons pour un utilisateur non autorisé de récupérer ou de créer un SID d’objet source souhaité, l’utilisateur non autorisé ne peut pas l’utiliser pour mettre à jour le <strong>SIDHistory</strong> d’un compte sans être membre du groupe administrateurs de domaine de destination. Étant donné que la vérification, sur le contrôleur de domaine de destination, pour l’appartenance à un administrateur de domaine est codée en dur, sur le contrôleur de domaine cible, il n’existe aucune méthode permettant d’effectuer une modification de disque pour modifier les données de contrôle d’accès qui protègent cette fonction. Une tentative de clonage d’un compte source cheval de Troie est auditée dans le domaine de destination. Cette attaque est atténuée en réservant l’appartenance au groupe administrateurs de domaine uniquement pour les personnes hautement fiables.<br /> | 
| Modification sur disque de l’historique SID<br /> Un utilisateur non autorisé sophistiqué, avec des informations d’identification d’administrateur de domaine et ayant un accès physique à un contrôleur de domaine dans le domaine de destination, peut modifier une valeur <strong>SIDHistory</strong> de compte sur le disque.<br /> | Cette tentative n’est pas activée à l’aide de <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>. Cette attaque est atténuée en empêchant l’accès physique aux contrôleurs de domaine, à l’exception des administrateurs hautement approuvés.<br /> | 
| Code non autorisé utilisé pour supprimer les protections<br /> Un utilisateur non autorisé ou un administrateur malveillant disposant d’un accès physique au code du service d’annuaire pourrait créer du code non autorisé :<ol><li>Supprime la vérification de l’appartenance au groupe administrateurs de domaine dans le code.</li><li>Modifie les appels sur le contrôleur de domaine source qui pointe le SID sur un LookupSidFromName qui n’est pas audité.</li><li>Supprime les appels du journal d’audit.</li></ol><br /> | Une personne ayant un accès physique au code du service d’annuaire et suffisamment compétent pour créer du code non fiable a la possibilité de modifier arbitrairement l’attribut <strong>SIDHistory</strong> d’un compte. L’API <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> n’augmente pas ce risque de sécurité.<br /> | 
| Ressources vulnérables aux sid volés<br /> Si un utilisateur non autorisé a réussi à utiliser l’une des méthodes décrites ici pour modifier un compte <strong>SIDHistory</strong>de compte, et si les domaines de ressources dignes d’intérêt approuvent le domaine de compte d’utilisateur non autorisé, l’utilisateur non autorisé peut accéder aux ressources du SID volé, éventuellement sans quitter une piste d’audit dans le domaine de compte à partir duquel le SID a été volé.<br /> | Les administrateurs de domaine de ressources protègent leurs ressources en configurant uniquement les relations d’approbation qui sont logiques du point de vue de la sécurité. L’utilisation de <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> est limitée, dans le domaine cible approuvé, aux membres du groupe administrateurs de domaine qui possèdent déjà des autorisations étendues dans le cadre de leurs responsabilités.<br /> | 
| Domaine cible non autorisé<br /> un utilisateur non autorisé crée un domaine Windows 2000 avec un compte dont le <strong>sIDHistory</strong> contient un SID qui a été volé à partir d’un domaine source. L’utilisateur non autorisé utilise ce compte pour un accès non autorisé aux ressources.<br /> | L’utilisateur non autorisé requiert des informations d’identification d’administrateur pour le domaine source afin d’utiliser <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>et laisse une piste d’audit sur le contrôleur de domaine source. Le domaine cible non autorisé bénéficie d’un accès non autorisé uniquement dans les autres domaines qui approuvent le domaine non autorisé, ce qui requiert des privilèges d’administrateur dans ces domaines de ressources.<br /> | 




 

## <a name="operational-constraints"></a>Contraintes opérationnelles

Cette section décrit les contraintes opérationnelles liées à l’utilisation de la fonction [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) .

Le SID de *SrcPrincipal* ne doit pas déjà exister dans la forêt de destination, qu’il s’agisse d’un SID de compte principal ou de l' **attribut sIDHistory** d’un compte. L’exception est que [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ne génère pas d’erreur lors de la tentative d’ajout d’un SID à un **SIDHistory** qui contient un SID identique. Ce comportement permet à **DsAddSidHistory** de s’exécuter plusieurs fois avec une entrée identique, ce qui aboutit à la réussite et à un état final cohérent, pour faciliter l’utilisation des développeurs d’outils.

> [!Note]  
> La latence de réplication du catalogue global peut fournir une fenêtre pendant laquelle des SID dupliqués peuvent être créés. Toutefois, les SID dupliqués peuvent être facilement supprimés par un administrateur.

 

*SrcPrincipal* et *DstPrincipal* doivent être de l’un des types suivants :

-   Utilisateur
-   Groupe avec sécurité activée, y compris :

    <dl> Groupe local  
    Groupe global  
    groupe de domaine local (Windows 2000 en mode natif uniquement)  
    groupe universel (Windows 2000 en mode natif uniquement)  
    </dl>

Les types d’objets de *SrcPrincipal* et *DstPrincipal* doivent correspondre.

-   Si *SrcPrincipal* est un utilisateur, *DstPrincipal* doit être un utilisateur.
-   Si *SrcPrincipal* est un groupe local ou de domaine local, *DstPrincipal* doit être un groupe de domaine local.
-   Si *SrcPrincipal* est un groupe global ou universel, *DstPrincipal* doit être un groupe global ou universel.

*SrcPrincipal* et *DstPrincipal* ne peuvent pas être de l’un des types suivants : ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) échoue avec une erreur dans ces cas)

-   Ordinateur (station de travail ou contrôleur de domaine)
-   Approbation inter-domaines
-   Compte dupliqué temporaire (fonctionnalité presque inutilisée, ancien élément LANman)
-   Comptes avec des SID bien connus. Les SID bien connus sont identiques dans chaque domaine ; par conséquent, l’ajout de ces éléments à un **sIDHistory** violerait l’exigence d’unicité SID d’une forêt Windows 2000. Les comptes avec des SID bien connus incluent les groupes locaux suivants :

    <dl> Opérateurs de compte  
    Administrateurs  
    Opérateurs de sauvegarde  
    Invités  
    Opérateurs d’impression  
    Duplicateur  
    Opérateurs de serveur  
    Utilisateurs  
    </dl>

Si *SrcPrincipal* a un identificateur relatif connu (RID) et un préfixe spécifique à un domaine, c’est-à-dire les administrateurs de domaine, les utilisateurs de domaine et les ordinateurs du domaine, *DstPrincipal* doit posséder le même RID bien connu pour que [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) puisse fonctionner correctement. Les comptes avec des RID bien connus incluent les utilisateurs et les groupes globaux suivants :

-   Administrateur
-   Invité
-   Administrateurs de domaine
-   Invités du domaine
-   Utilisateurs du domaine

## <a name="setting-the-registry-value"></a>Définition de la valeur de Registre

La procédure suivante montre comment définir la valeur de registre TcpipClientSupport.

**Pour définir la valeur de registre TcpipClientSupport**

1.  Créez la valeur de Registre suivante en tant que \_ valeur reg DWORD sur le contrôleur de domaine source et définissez sa valeur sur 1.

    **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôle \\ LSA \\ TcpipClientSupport**

2.  Ensuite, redémarrez le contrôleur de domaine source. Cette valeur de registre fait en sorte que le SAM écoute le protocole TCP/IP. [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) échoue si cette valeur n’est pas définie sur le contrôleur de domaine source.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Activation de l’audit des événements de gestion des utilisateurs/groupes

la procédure suivante montre comment activer l’audit des événements de gestion des utilisateurs/groupes dans un domaine Windows 2000 ou Windows Server 2003 source ou de destination.

**pour activer l’audit des événements de gestion des utilisateurs/groupes dans un domaine Windows 2000 ou Windows Server 2003 source ou destination**

1.  Dans le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory, sélectionnez le conteneur contrôleurs de domaine de domaine de destination.
2.  Cliquez avec le bouton droit sur **contrôleurs de domaine** , puis choisissez **Propriétés**.
3.  Cliquez sur l’onglet **stratégie de groupe** .
4.  Sélectionnez la **stratégie contrôleurs de domaine par défaut** et cliquez sur **modifier**.
5.  sous **Configuration ordinateur \\ Windows Paramètres \\ sécurité Paramètres \\ \\ stratégie d’audit stratégies locales**, double-cliquez sur **auditer la gestion des comptes**.
6.  Dans la fenêtre **auditer la gestion des comptes** , sélectionnez audit des **réussites** et des **échecs** . Les mises à jour de stratégie prennent effet après un redémarrage ou après l’actualisation.
7.  Vérifiez que l’audit est activé en affichant la stratégie d’audit effective dans le composant logiciel enfichable MMC stratégie de groupe.

La procédure suivante montre comment activer l’audit des événements de gestion des utilisateurs/groupes dans un domaine Windows NT 4,0.

**Pour activer l’audit des événements de gestion des utilisateurs/groupes dans un domaine Windows NT 4,0**

1.  Dans le **Gestionnaire des utilisateurs pour les domaines**, cliquez sur le menu **stratégies** et sélectionnez **audit**.
2.  Sélectionnez **auditer ces événements**.
3.  Pour la **gestion des utilisateurs et des groupes**, vérifiez la **réussite et l’échec**.

la procédure suivante montre comment activer l’audit des événements de gestion des utilisateurs/groupes dans un domaine source Windows NT 4,0, Windows 2000 ou Windows Server 2003.

**pour activer l’audit des événements de gestion des utilisateurs/groupes dans un domaine source Windows NT 4,0, Windows 2000 ou Windows Server 2003**

1.  Dans le **Gestionnaire des utilisateurs pour les domaines**, cliquez sur le menu **utilisateur** , puis sélectionnez **nouveau groupe local**.
2.  Entrez un nom de groupe composé du nom NetBIOS du domaine source, à l’aide de trois signes dollar ($), par exemple, FABRIKAM $ $ $. Le champ description doit indiquer que ce groupe est utilisé pour auditer l’utilisation des [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ou des opérations de clonage. Assurez-vous qu’il n’y a aucun membre dans le groupe. Cliquez sur **OK**.

L’opération [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) échoue si l’audit de source et de destination n’est pas activé comme décrit ici.

## <a name="set-up-trust-if-required"></a>Configurer l’approbation si nécessaire

Si l’une des conditions suivantes est vraie, une approbation doit être établie entre le domaine source et le domaine de destination (cela doit se produire dans une autre forêt) :

-   le domaine source est Windows Server 2003.
-   Le domaine source est Windows NT 4,0 et *SrcDomainCreds* a la **valeur null**.

 

 





