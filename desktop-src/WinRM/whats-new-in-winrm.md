---
title: Nouveautés de WinRM 2,0
description: de nouvelles fonctionnalités sont disponibles dans Windows Remote Management version 2,0. (WinRM 2,0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d322b0b86600cd783bd787427b53df334f3d499a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480585"
---
# <a name="whats-new-in-winrm-20"></a>Nouveautés de WinRM 2,0

de nouvelles fonctionnalités sont disponibles dans Windows Remote Management version 2,0. (WinRM 2,0)

WinRM 2,0 est inclus dans Windows Server 2008 R2 et Windows 7.

vous pouvez également télécharger WinRM 2,0 pour Windows Server 2008 avec service pack 2 (sp2) et Windows Vista avec service pack 2 (sp2). Pour plus d’informations sur le téléchargement de WinRM 2,0, voir [l’article KB968929](https://support.microsoft.com/kb/968929).

Le tableau suivant répertorie la documentation de WinRM 2,0.




| Rubrique | Description | 
|-------|-------------|
| <a href="client-shell-api.md">API du shell client WinRM</a><br /> | L’interface de programmation d’applications (API) du shell client WinRM fournit des fonctionnalités permettant de créer et de gérer des shells et des opérations de Shell, des commandes et des flux de données sur des ordinateurs distants. <br /> | 
| <a href="winrm-plugin-api.md">API de plug-in WinRM</a><br /> | L’API de plug-in WinRM fournit des fonctionnalités qui permettent à un utilisateur d’écrire des plug-ins en implémentant certaines API pour les opérations et les <a href="windows-remote-management-glossary.md"><em>URI de ressources</em></a> pris en charge.<br /> | 
| <a href="winrm-application-hosting.md">Infrastructure pour la gestion des services hébergés</a><br /> | WinRM 2,0 introduit un Framework d’hébergement. Deux modèles d’hébergement sont pris en charge. L’une est basée sur Internet Information Services (IIS), et l’autre sur WinRM – service. <br /> Pour plus d’informations sur la configuration de l’hôte, consultez les rubriques suivantes :<br /><ul><li><a href="iis-host-plug-in-configuration.md">Configuration du plug-in hôte IIS</a></li><li><a href="wsman-service-plug-in-configuration.md">Configuration du plug-in du service WinRM</a></li></ul> | 
| <a href="dmtf-association-traversal.md">Découverte de profil DMTF par traversée d’association</a><br /> | La traversée d’association permet à un utilisateur de récupérer des instances de classes d’association à l’aide d’un mécanisme de filtrage standard.<br /> | 
| <a href="remote-shell-infrastructure-improvements.md">Améliorations de l’infrastructure du shell distant</a><br /> | Cette rubrique contient des informations sur les améliorations apportées à l’infrastructure à distance pour WinRM. <br /> | 
| <a href="multi-hop-support.md">Prise en charge de plusieurs tronçons</a><br /> | La fonctionnalité a été ajoutée à WinRM 2,0 qui prend en charge la délégation des informations d’identification de l’utilisateur sur plusieurs ordinateurs distants. <br /> La rubrique sur les <a href="authentication-constants.md"><strong>constantes d’authentification</strong></a> a été mise à jour pour ajouter la constante suivante : <strong>WSManFlagUseCredSsp</strong>.<br /> L’API C++ suivante a été ajoutée pour assurer la prise en charge de plusieurs tronçons : <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br /> L’API de script suivante a été ajoutée pour assurer la prise en charge de plusieurs tronçons : <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. SessionFlagUseCredSsp</strong></a>.<br /> | 
| <a href="quotas.md">Gestion des quotas pour les shells distants</a><br /> | Cette rubrique contient des informations sur la configuration des quotas pour la gestion des shells à distance.<br /> | 
| <a href="winrm-powershell-commandlets.md">Référence managée pour les commandes WS-Management PowerShell</a><br /> | les utilisateurs de WinRM 2,0 peuvent utiliser des applets de commande Windows PowerShell pour la gestion du système.<br /> | 




 

 

 





