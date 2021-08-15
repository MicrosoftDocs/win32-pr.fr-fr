---
description: Les fonctions suivantes sont utilisées avec l’échange de réseau.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Fonctions DDE réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b37e83dd6b335e1acd2e77010fa61d0da5e3e26af5b46eef54d5ee20cf2eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756308"
---
# <a name="network-dde-functions"></a>Fonctions DDE réseau

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Les fonctions suivantes sont utilisées avec l’échange de réseau.



| Fonction                                                   | Description                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Convertit un code d’erreur retourné par une fonction DDE réseau en une chaîne d’erreur qui explique le code d’erreur retourné. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Récupère le descripteur de sécurité associé au partage DDE.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Récupère les options associées à un partage DDE figurant dans la liste des partages approuvés de l’utilisateur du serveur.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Détermine si une application et une chaîne de rubrique («*appname* \| *thème*») utilisent la syntaxe appropriée.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Détermine si un nom de partage utilise la syntaxe appropriée.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Définit le descripteur de sécurité associé au partage DDE.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Octroie l’état de confiance du partage DDE spécifié dans le contexte de l’utilisateur actuel.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Crée et ajoute un nouveau partage DDE au gestionnaire de base de données du partage DDE (DSDM).                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Supprime un partage DDE du DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Récupère la liste des partages DDE disponibles.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Récupère les informations de partage DDE.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Définit les informations de partage DDE.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Récupère les noms de tous les partages DDE réseau approuvés dans le contexte du processus appelant.                 |



 

 

 



