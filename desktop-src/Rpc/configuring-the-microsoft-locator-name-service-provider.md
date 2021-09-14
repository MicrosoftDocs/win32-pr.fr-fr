---
title: Configuration du fournisseur de services Microsoft Locator Name
description: Vous pouvez modifier le fournisseur de services de noms que vous avez spécifié en modifiant le fichier de configuration Rpcreg. dat, qui contient les paramètres NSP et les paramètres de protocole RPC. Utilisez un éditeur de texte pour modifier les entrées NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233490"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a>Configuration du fournisseur de services Microsoft Locator Name

Vous pouvez modifier le fournisseur de services de noms que vous avez spécifié en modifiant le fichier de configuration Rpcreg. dat, qui contient les paramètres NSP et les paramètres de protocole RPC. Utilisez un éditeur de texte pour modifier les entrées NSP.

**Pour reconfigurer le fournisseur de services de noms Microsoft Locator**

1.  Ouvrez le fichier Rpcreg. dat à l’aide d’un éditeur de texte.

    Rpcreg. dat se trouve dans le répertoire racine, sauf si vous avez spécifié un chemin d’accès différent au cours de l’installation.

2.  Définissez les valeurs suivantes pour les entrées de registre. 

    | Entrée de Registre                                         | Valeur                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \\Protocole Microsoft \\ RPC \\ NameService \\       | Séquence de protocole pour le protocole que vous utilisez. La valeur par défaut est **ncacn \_ NP**.                                                                   |
    | Logiciel \\ Microsoft \\ RPC \\ NameService \\ networkAddress | Nom de l’ordinateur exécutant le localisateur qui est utilisé par les clients lors des opérations de recherche du service de nom. La valeur par défaut est le contrôleur de domaine principal. |
    | \\Point de \\ \\ terminaison NameService Microsoft RPC \\ logiciel       | Nom du point de terminaison utilisé par le service de noms. La valeur par défaut est le \\ localisateur de canal \\ .                                                                    |

    

     

3.  Enregistrez et fermez le fichier.

 

 




