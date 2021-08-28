---
title: Conversion des formats de nom de compte de domaine
description: Les fonctions Microsoft Win32 permettant d’utiliser le gestionnaire de contrôle des services (SCM) sur un serveur hôte utilisent le \ 0034 ; \\ nom d’utilisateur de domaine \ 0034 ; format pour les comptes de service.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa1b3664cc0ad372f82b498153862e69013fb1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881608"
---
# <a name="converting-domain-account-name-formats"></a>Conversion des formats de nom de compte de domaine

Les fonctions Microsoft Win32 permettant d’utiliser le gestionnaire de contrôle des services (SCM) sur un serveur hôte utilisent le &lt; format « domaine &gt; \\ &lt; nom_utilisateur &gt; » pour les comptes de service. Par exemple, si vous appelez la fonction [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) pour récupérer le compte d’utilisateur sous lequel votre service s’exécute, la fonction retourne le nom dans le format « Fabrikam \\ JeffSmith ». Pour effectuer une liaison au compte d’utilisateur dans l’annuaire, par exemple pour modifier le mot de passe du compte, le nom unique du compte est requis, dont le format est « CN = Jeff Smith, CN = Users, DC = fabrikam, DC = COM ».

Pour effectuer une conversion entre les différents formats de noms, utilisez la fonction [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) , qui peut convertir un nom dans d’autres formats, par exemple un nom d’utilisateur principal (UPN).

 

 
