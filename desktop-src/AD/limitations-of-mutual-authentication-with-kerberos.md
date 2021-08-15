---
title: Limitations de l’authentification mutuelle avec Kerberos
description: le compte du client et le compte du service doivent être en 2000 Windows de domaines natifs ou en mode mixte, car les services Kerberos ne sont pas disponibles dans les domaines de niveau inférieur.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bdc2f8cfe87d3cece32987ee0958000b1186775257013ce27f5950c6ac8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187063"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Limitations de l’authentification mutuelle avec Kerberos

le compte du client et le compte du service doivent être en 2000 Windows de domaines natifs ou en mode mixte, car les services Kerberos ne sont pas disponibles dans les domaines de niveau inférieur. En outre, les comptes de service et de client doivent se trouver dans la même forêt, car le KDC du client utilise le catalogue global pour rechercher le nom de principal du service.

le service et le client doivent s’exécuter sur Windows 2000, sinon l’authentification mutuelle avec kerberos échouera, car les versions antérieures de Windows ne prennent pas en charge kerberos.

Les noms de principal du service doivent inclure le nom DNS du serveur hôte sur lequel le service s’exécute. Vous devez utiliser le nom DNS.

 

 




