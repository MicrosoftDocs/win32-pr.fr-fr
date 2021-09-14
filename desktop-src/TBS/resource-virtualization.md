---
title: Virtualisation des ressources
description: Virtualisation des ressources
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193620"
---
# <a name="resource-virtualization"></a>Virtualisation des ressources

La fonction principale du TBS est de partager efficacement certaines ressources TPM limitées : clés, autorisation et sessions de transport.

Lorsqu’une instance de l’une de ces ressources est créée, le TBS crée une instance virtuelle de la ressource et retourne un descripteur de cette instance virtuelle dans le flux de commandes de résultat (plutôt que l’instance de handle réelle retournée par le module de plateforme sécurisée). Le TBS maintient un mappage entre le descripteur virtuel et le handle réel en interne. Si le module de plateforme sécurisée manque d’espace pour contenir plus de ressources d’un type donné, les instances existantes de la ressource sont enregistrées et supprimées de manière sélective jusqu’à ce que le module de plateforme sécurisée puisse contenir la nouvelle ressource. Lorsque les anciennes ressources sont à nouveau nécessaires, le TBS charge les contextes enregistrés (en enregistrant et en excluant d’autres ressources si nécessaire) avant d’envoyer la commande.

Toute la virtualisation dans le TBS est effectuée pour le compte d’un contexte spécifique. Chaque contexte est uniquement autorisé à accéder à des ressources virtuelles créées spécifiquement en son nom, ainsi qu’à des ressources physiques sur le module de plateforme sécurisée qui correspond à ces ressources virtuelles. Par défaut, le nombre total de toutes les ressources virtualisées est limité à 500. Ce nombre peut être modifié en créant ou en modifiant une valeur de Registre **DWORD** nommée **MaxResources** sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **TPM**. L’utilisation des ressources TBS en temps réel peut être observée à l’aide de l’outil Analyseur de performances pour suivre le nombre de ressources TBS. cette restriction est devenue obsolète avec Windows 8 et Windows Server 2012.

Les ressources TPM limitées qui ne sont pas virtualisées par le TBS (tels que les compteurs et le magasin NV) doivent être partagées de manière coopérative entre les piles logicielles.

> [!Note]  
> Cette virtualisation de handle entraîne l’échec des commandes qui incluent des handles de clé dans le calcul de paramètres d’autorisation HMAC. Par conséquent, de nombreuses commandes dépréciées dans la version 1,2 du module de plateforme sécurisée ne peuvent pas être utilisées par les logiciels d’application dans l’environnement TBS.

 

## <a name="resource-limits"></a>Limites de ressources

Le module de plateforme sécurisée permet aux appelants d’interroger ses fonctionnalités pour déterminer la quantité d’espace disponible pour certains types de ressources. Certaines de ces limites de ressources, telles que la quantité d’espace disponible pour les clés, les sessions d’autorisation et les sessions de transport, sont effectivement étendues par le TBS via la virtualisation. Les limitations de TBS, qui sont contrôlées par le paramètre de Registre **MaxResources** , sont généralement beaucoup plus volumineuses que les limitations réelles du matériel TPM sous-jacent. Aucun mécanisme n’est fourni pour interroger les limitations de TBS indépendamment des limites matérielles du module de plateforme sécurisée. cette limitation de TBS est devenue obsolète avec Windows 8 et Windows Server 2012.

## <a name="keys"></a>Keys

Le TBS virtualise les handles de clé afin que les clés puissent être déchargées de façon transparente à partir du module de plateforme sécurisée lorsqu’elles ne sont pas utilisées et rechargées dans le module de plateforme sécurisée lorsqu’elles sont nécessaires. Lorsqu’une clé est créée, le TBS associe un descripteur virtuel à la clé chargée. Le même descripteur virtuel est utilisé pour la durée de vie de la ressource. Les handles de clé virtuelle ne sont valides que dans le contexte qui les a créés et les ressources associées ne sont pas conservées au-delà de la durée de vie du contexte.

-   Création de clés avec TPM \_ LoadKey2

    Si une clé est créée à l’aide de la \_ commande TPM LoadKey2, TPM2 \_ CREATEPRIMARY, TPM2 \_ Load ou TPM2 \_ LoadExternal, le TBS remplace le handle dans le flux d’octets de retour par un handle de clé virtuelle de son choix. En conséquence, le TBS garantit que chaque descripteur virtuel est unique. Si le TBS détecte une collision (événement extrêmement peu probable), le TBS décharge la clé du module de plateforme sécurisée (TPM) et informe le logiciel appelant. Le logiciel peut ensuite soumettre à nouveau l’opération. Ce processus peut être répété jusqu’à ce que le TBS récupère un handle de clé unique.

-   Désactivation de clés

    Le service TBS invalide le descripteur de clé virtuelle lorsqu’il reçoit un \_ message FLUSHSPECIFIC TPM ou TPM2 \_ FlushContext pour ce descripteur virtuel du contexte client. Si la clé est physiquement présente dans le module de plateforme sécurisée lors de la réception du message de vidage, le TBS vide la clé du module de plateforme sécurisée à ce moment-là.

-   Suppression temporaire de clés

    Lors de la suppression d’une clé du module de plateforme sécurisée pour faire de la place pour un nouvel élément, le TBS exécute une \_ commande TPM SaveContext ou TPM2 \_ ContextSave sur la clé avant de la supprimer.

-   Restauration de clés

    Lorsqu’une commande qui fait référence à une clé chargée est soumise au TBS, elle garantit que la clé est physiquement présente dans le module de plateforme sécurisée. Si la clé n’est pas présente, le service TBS la restaure avec un appel à TPM \_ LoadContext ou TPM2 \_ ContextLoad. Si une clé ne peut pas être restaurée dans le module de plateforme sécurisée, le TBS retourne le module de plateforme sécurisé \_ E TPM E \_ non valide \_ en tant que résultat TPM.

Le TBS remplace chaque descripteur virtuel associé à une clé dans un flux de commande par le handle physique de la clé chargée sur le module de plateforme sécurisée. Si une commande est envoyée avec un handle virtuel qui n’est pas reconnu par le TBS dans le contexte de l’appelant, le TBS met en forme un flux d’erreur pour l’appelant avec le module de plateforme sécurisé \_ E TPM E \_ non valide \_ .

## <a name="authorization-sessions"></a>Sessions d’autorisation

Les sessions d’autorisation sont créées en appelant TPM \_ OIAP, TPM \_ osap ou TPM \_ DSAP. Dans chaque cas, le flux d’octets de retour contient le handle de module de plateforme sécurisée physique de la session d’autorisation nouvellement créée. Le TBS remplace ceci par un handle virtuel. Lorsque la session d’autorisation est ensuite référencée, le TBS remplace le descripteur virtuel dans le flux de commande par le handle physique de la session d’autorisation. Le TBS garantit que la durée de vie de la session d’autorisation virtuelle correspond à celle de la session d’autorisation physique. Si un client tente d’utiliser un descripteur virtuel expiré, le TBS formate un flux d’erreur avec l’erreur TPM \_ INVALIDAUTHHANDLE.

Les emplacements de session sont limités et le TBS peut manquer d’emplacements externes dans lesquels enregistrer les contextes de session d’autorisation. Dans ce cas, le TBS choisit une session d’autorisation à invalider afin que le nouveau contexte puisse être enregistré avec succès. Une application qui tente d’utiliser l’ancien contexte doit recréer la session d’autorisation.

Le TBS invalide la session d’autorisation virtuelle lorsque l’un des cas suivants se produit :

-   L’indicateur continue-use associé à la session d’autorisation dans le flux de commandes retourné à partir du module de plateforme sécurisée est **false**.
-   Une commande qui utilise une session d’autorisation échoue.
-   Une commande qui invalide la session d’autorisation associée à la commande (par exemple, CreateWrapKey TPM) est exécutée \_ .
-   Une clé associée à une session OSAP ou DSAP est supprimée du module de plateforme sécurisée avec un appel à TPM \_ FlushSpecific ou TPM2 \_ FlushContext (sans tenir compte du fait que cette commande provient du TBS ou d’un logiciel de niveau supérieur).

    Le TBS resynchronise automatiquement les sessions d’autorisation après l’exécution réussie de certaines commandes non déterministes pour s’assurer que l’état du TBS reste cohérent avec l’état du module de plateforme sécurisée (TPM). Les commandes affectées sont les suivantes :

    -   \_Gérer les \_ délégués TPM ORD \_
    -   \_CreateOwnerDelegation de \_ délégué TPM ORD \_
    -   \_LoadOwnerDelegation de \_ délégué TPM ORD \_

Dans chacun des cas suivants, la session d’autorisation sur le module de plateforme sécurisée est vidée automatiquement par le module de plateforme sécurisée :

-   Création de sessions d’autorisation

    Les handles de session d’autorisation virtuelle ne sont valides que dans le contexte qui les a créés et les ressources associées ne sont pas conservées au-delà de la durée de vie du contexte associé.

-   Suppression des sessions d’autorisation

    Le TBS invalide la session d’autorisation virtuelle si elle reçoit une commande TPM \_ FlushSpecific ou TPM2 \_ FlushContext pour le descripteur virtuel du contexte client. Si la session d’autorisation est physiquement présente dans le module de plateforme sécurisée lors de la réception de la commande flush, le TBS vide immédiatement la session physique du module de plateforme sécurisée.

-   Supprimer temporairement des sessions d’autorisation

    Lorsque vous supprimez une session d’autorisation du module de plateforme sécurisée pour faire de la place pour une nouvelle entité, le TBS exécute le module de plateforme sécurisée \_ SaveContext ou TPM2 \_ ContextSave sur cette session d’autorisation.

-   Restauration des sessions d’autorisation

    Lorsqu’une commande GPC autorisée est soumise au TBS, le TBS s’assure que toutes les sessions d’autorisation virtuelles référencées dans la commande sont physiquement présentes sur le module de plateforme sécurisée. Si l’une des sessions d’autorisation n’est pas présente, le TBS les restaure à l’aide d’un appel à TPM \_ LoadContext ou TPM2 \_ ContextLoad. Si une session d’autorisation ne peut pas être restaurée dans le module de plateforme sécurisée, le TBS retourne le \_ handle TPM E \_ non valide \_ comme résultat du module de plateforme sécurisée.

Le TBS remplace chaque descripteur virtuel associé à une session d’autorisation dans un flux de commande par le handle physique de la session d’autorisation chargée sur le module de plateforme sécurisée.

Si une commande est envoyée avec un descripteur virtuel qui n’est pas reconnu par le TBS dans le contexte de l’appelant, le TBS met en forme un flux d’erreur pour l’appelant avec le \_ \_ descripteur non valide d’erreur TPM E \_ .

## <a name="transport-sessions"></a>Sessions de transport

> [!Note]  
> la gestion des sessions de transport, comme décrit ici, est spécifique à Windows Vista et Windows Server 2008.

 

Les sessions de transport sont un mécanisme fourni par le module de plateforme sécurisée qui permet à une pile de logiciels de chiffrer les données dans une commande à mesure qu’elles transitent entre le logiciel et le module de plateforme sécurisée. Cela empêche un adversaire d’intercepter les données lorsqu’elles sont transmises sur le bus matériel.

> [!IMPORTANT]
> Seules les données de charge utile sont chiffrées. Les commandes en cours d’exécution peuvent toujours être identifiées.

 

Malheureusement, ce mécanisme empêche également le TBS d’examiner les données de charge utile. Dans la plupart des cas, ce n’est pas un problème car le TBS modifie uniquement les descripteurs, pas les données de charge utile. Toutefois, dans le cas de TPM \_ LoadContext par exemple, le descripteur de ressource retourné est couvert par le chiffrement. Par conséquent, le service TBS empêche toute tentative d’exécution d’une \_ opération LOADCONTEXT TPM couverte par une session de transport.

Le TBS bloque les commandes suivantes dans la session de transport :

-   \_ESTABLISHTRANSPORT TPM
-   \_EXECUTETRANSPORT TPM
-   \_Handle de terminaison TPM \_
-   \_LOADKEY TPM
-   \_EVICTKEY TPM
-   \_SAVEKEYCONTEXT TPM
-   \_LOADKEYCONTEXT TPM
-   \_SAVEAUTHCONTEXT TPM
-   \_LOADAUTHCONTEXT TPM
-   \_SAVECONTEXT TPM
-   \_LOADCONTEXT TPM
-   \_FLUSHSPECIFIC TPM

Quand l’une de ces commandes est couverte par une session de transport, le TBS retourne \_ la \_ commande TPM E Embedded \_ \_ non prise en charge en tant que résultat du module de plateforme sécurisée.

Les handles de session de transport sont virtualisés d’une manière similaire aux handles de clé et d’autorisation. Un nombre limité d’emplacements de contexte de session de transport enregistrés sont disponibles sur le module de plateforme sécurisée.

Le TBS invalide la session de transport virtuel si l’un des cas suivants se produit :

-   L’indicateur continue-use associé à la session de transport dans le flux de commandes de retour du module de plateforme sécurisée a la **valeur false**.

    Comme avec les sessions d’autorisation ci-dessus, le TBS resynchronise automatiquement les sessions de transport après l’exécution réussie de certaines commandes non déterministes pour s’assurer que l’état de TBS reste cohérent avec l’état du module de plateforme sécurisée. Les commandes affectées sont les suivantes :

    -   \_Gérer les \_ délégués TPM ORD \_
    -   \_CreateOwnerDelegation de \_ délégué TPM ORD \_
    -   \_LoadOwnerDelegation de \_ délégué TPM ORD \_

Dans chacun de ces cas, la session de transport sur le module de plateforme sécurisée est vidée automatiquement par le module de plateforme sécurisée :

-   Création de sessions de transport

    Le TBS crée un descripteur virtuel pour chaque session de transport créée par un client. Les descripteurs de transport virtuels sont uniquement valides dans le contexte qui les a créés et les ressources associées ne sont pas conservées au-delà de la durée de vie du contexte associé.

-   Désactivation des sessions de transport

    Le TBS invalide la session de transport virtuel si elle reçoit une commande TPM \_ FlushSpecific pour le descripteur virtuel du contexte client. Si la session de transport est physiquement présente dans le module de plateforme sécurisée lors de la réception de la commande flush, le TBS vide immédiatement la session physique du module de plateforme sécurisée.

-   Supprimer temporairement les sessions de transport

    Lors de la suppression d’une session de transport du module de plateforme sécurisée pour faire de la place pour une nouvelle entité, le TBS exécute le module de plateforme sécurisée \_ SaveContext sur cette session de transport.

-   Restauration des sessions de transport

    Lorsqu’une \_ commande EXECUTETRANSPORT TPM est soumise au tbs, le TBS garantit que la session de transport référencée dans la commande est physiquement présente sur le module de plateforme sécurisée. Si la session de transport n’est pas présente, le service TBS la restaure avec un appel à TPM \_ LoadContext.

Le TBS remplace le descripteur virtuel associé à la session de transport dans un flux de commande par le handle physique de la session de transport chargée sur le module de plateforme sécurisée. Si une commande est envoyée avec un descripteur virtuel qui n’est pas reconnu par le TBS dans le contexte de l’appelant, le TBS formate un flux d’erreur pour l’appelant à l’aide du \_ handle TPM E \_ non valide \_ .

## <a name="exclusive-transport-sessions"></a>Sessions de transport exclusives

Les sessions de transport encapsulées exclusives sont un moyen pour les logiciels de niveau supérieur de déterminer si un autre logiciel a accédé au module de plateforme sécurisée pendant une chaîne de commandes. Ils n’empêchent pas d’autres logiciels d’accéder au module de plateforme sécurisée (TPM), ils accordent simplement au créateur de la session de transport un moyen de déterminer qu’un autre accès a eu lieu. Le service TBS n’effectue aucune action spécifique pour empêcher les sessions de transport exclusives, mais il est quelque peu incompatible avec eux. Le service TBS tente de dupliquer le comportement naturel du module de plateforme sécurisée en étant transparent, il ne favorise donc pas les commandes des contextes qui établissent une session de transport exclusive. Par exemple, si le client B envoie une commande lorsque le client A est dans une session de transport exclusive, il invalidera la session de transport exclusive du client A.

Les commandes lancées par TBS peuvent également mettre fin à la session de transport exclusive. Cela se produit lorsque le client A est dans une session de transport exclusive et qu’une commande exécutée par le client A appelle pour une ressource qui n’est pas physiquement présente dans le module de plateforme sécurisée. Cette situation déclenche le gestionnaire de virtualisation TBS pour exécuter une commande TPM \_ LoadContext afin de fournir cette ressource, qui met fin à la session de transport exclusive du client a.

 

 




