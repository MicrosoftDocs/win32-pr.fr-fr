---
title: Limitations de l’authentification mutuelle avec Kerberos
description: Le compte du client et le compte du service doivent être dans des domaines Windows 2000 natifs ou en mode mixte, car les services Kerberos ne sont pas disponibles dans les domaines de niveau inférieur.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462015"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Limitations de l’authentification mutuelle avec Kerberos

Le compte du client et le compte du service doivent être dans des domaines Windows 2000 natifs ou en mode mixte, car les services Kerberos ne sont pas disponibles dans les domaines de niveau inférieur. En outre, les comptes de service et de client doivent se trouver dans la même forêt, car le KDC du client utilise le catalogue global pour rechercher le nom de principal du service.

Le service et le client doivent s’exécuter sur Windows 2000. dans le cas contraire, l’authentification mutuelle avec Kerberos échouera, car les versions antérieures de Windows ne prendront pas en charge Kerberos.

Les noms de principal du service doivent inclure le nom DNS du serveur hôte sur lequel le service s’exécute. Vous devez utiliser le nom DNS.

 

 




