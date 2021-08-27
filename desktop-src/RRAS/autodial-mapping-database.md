---
title: Base de données de mappage de numérotation automatique
description: La base de données de mappage de la numérotation automatique mappe des adresses réseau à des entrées d’annuaire téléphonique RAS.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e89bd065a136492281adb3424636a8820c76c76bf6867e70db75aecfa0f345d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036719"
---
# <a name="autodial-mapping-database"></a>Base de données de mappage de numérotation automatique

La base de données de mappage de la numérotation automatique mappe des adresses réseau à des entrées d’annuaire téléphonique RAS. La base de données peut inclure des adresses IP (par exemple, « 172.21.167.35 »), des noms d’hôtes Internet (par exemple, « www.microsoft.com ») ou des noms NetBIOS (par exemple, « products1 »). Un ensemble d’une ou plusieurs entrées [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) sont associées à chaque adresse de la base de données de numérotation automatique. Chacune de ces entrées spécifie une entrée d’annuaire téléphonique que RAS peut composer pour se connecter à l’adresse à partir d’un emplacement de numérotation TAPI (Telephony Application Programming Interface) particulier. Pour plus d’informations sur les emplacements de numérotation TAPI, consultez la documentation relative à TAPI.

La numérotation automatique crée automatiquement des entrées dans la base de données de mappage de la numérotation automatique dans deux cas :

-   En cas d’échec d’une tentative de connexion à une adresse réseau

    S’il n’existe aucune entrée pour l’adresse dans la base de données de mappage et que l’ordinateur n’est pas connecté à un réseau, soit directement, soit via RAS, AutoDial invite l’utilisateur à spécifier les informations nécessaires pour établir une connexion d’accès à distance. Si l’utilisateur fournit les informations et que l’opération de connexion d’accès à distance est réussie, la numérotation automatique stocke les informations dans la base de données de mappage.

-   Lorsque l’ordinateur est connecté à un réseau via RAS

    Chaque fois que l’utilisateur se connecte à une adresse réseau, la numérotation automatique crée une entrée dans la base de données. L’entrée mappe l’adresse réseau à l’entrée de l’annuaire téléphonique qui a été utilisée pour établir la connexion RAS.

Vous pouvez utiliser la fonction [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) pour ajouter une adresse à la base de données de mappage de numérotation automatique, supprimer une adresse de la base de données ou modifier les entrées de numérotation automatique associées à une adresse existante dans la base de données. Vous pouvez utiliser la fonction [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) pour récupérer les entrées de numérotation automatique associées à une adresse réseau spécifiée dans la base de données de mappage de la numérotation automatique. La fonction [**RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) retourne une liste de toutes les adresses dans la base de données de mappage de la numérotation automatique.

 

 