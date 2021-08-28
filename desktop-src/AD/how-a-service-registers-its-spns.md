---
title: Comment un service enregistre ses SPN
description: Avant qu’un client puisse utiliser un SPN pour authentifier une instance d’un service, le SPN doit être inscrit sur le compte d’utilisateur ou d’ordinateur que l’instance de service utilisera pour ouvrir une session.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Comment un service inscrit sa publicité SPN
- nom de principal du service AD, comment un service enregistre ses SPN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93609ba6205c8075c81204ba5a614a9573d8da5a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881406"
---
# <a name="how-a-service-registers-its-spns"></a>Comment un service enregistre ses SPN

Avant qu’un client puisse utiliser un SPN pour authentifier une instance d’un service, le SPN doit être inscrit sur le compte d’utilisateur ou d’ordinateur que l’instance de service utilisera pour ouvrir une session. En règle générale, l’inscription du SPN est effectuée par un programme d’installation de service s’exécutant avec des privilèges d’administrateur de domaine.

Le programme d’installation du service qui installe une instance de service sur un ordinateur hôte effectue généralement la procédure suivante.

**Pour inscrire des SPN pour une instance de service**

1.  Appelez la fonction [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) pour créer un ou plusieurs SPN uniques pour l’instance de service. Pour plus d’informations, consultez [formats de noms pour les noms de principal du service uniques](name-formats-for-unique-spns.md).
2.  Appelez la fonction [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) pour enregistrer les noms sur le compte d’ouverture de session du service.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) inscrit des noms de principal du service en tant que propriété d’un objet de compte d’utilisateur ou d’ordinateur dans l’annuaire. les objets **utilisateur** et **ordinateur** ont un attribut **servicePrincipalName** , qui est un attribut à valeurs multiples pour le stockage de tous les noms de principal du service associés à un compte d’utilisateur ou d’ordinateur. Si le service s’exécute sous un compte d’utilisateur, les noms de principal du service sont stockés dans l’attribut **servicePrincipalName** de ce compte. Si le service s’exécute dans le compte LocalSystem, les noms de principal du service sont stockés dans l’attribut **servicePrincipalName** du compte de l’ordinateur hôte du service. L’appelant **DsWriteAccountSpn** doit spécifier le nom unique de l’objet de compte sous lequel les noms de principal du service sont stockés.

Pour vous assurer que les noms de principal du service inscrits sont sécurisés, l’attribut **servicePrincipalName** ne peut pas être écrit directement. Il peut uniquement être écrit en appelant [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna). L’appelant doit disposer d’un accès en écriture à l’attribut **servicePrincipalName** du compte cible. En règle générale, l’accès en écriture est accordé par défaut uniquement aux administrateurs de domaine. Toutefois, il existe un cas particulier dans lequel le système autorise un service s’exécutant sous le compte LocalSystem à inscrire ses propres noms de principal du service sur le compte d’ordinateur de l’hôte du service. Dans ce cas, le SPN en cours d’écriture doit avoir la forme « <service class> / &lt; host &gt; » et « &lt; host &gt; » doit être le nom DNS de l’ordinateur local.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) peut également supprimer des SPN d’un compte. Un paramètre d’opération indique si les noms de principal du service doivent être ajoutés au compte, supprimés du compte ou utilisés pour remplacer complètement tous les SPN actuels pour le compte. Quand une instance de service est désinstallée, supprimez tous les SPN inscrits pour cette instance.

Pour plus d’informations et pour obtenir un exemple de code qui inscrit ou annule l’enregistrement des noms principaux de service d’un service, consultez [enregistrement des noms principaux de service pour un service](registering-the-spns-for-a-service.md).

Les services basés sur l’hôte qui utilisent le format simple SPN « <service class> / &lt; host &gt; », ont la possibilité d’utiliser la fonction [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) , qui crée et inscrit les noms de principal du service pour une instance de service. **DsServerRegisterSpn** est une fonction d’assistance qui appelle [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) et [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna).

Pour plus d’informations, consultez [comptes d’ouverture de session du service](service-logon-accounts.md).

 

 




