---
description: Utilisez les commandes MakeCert pour créer des certificats de test à l’aide des options disponibles avec Internet Explorer version 4,0 ou ultérieure.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Utilisation de MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321eccfc26e3fc5bf13a541e1aab6a41b3f5d0930beed03f6033211bf63ac689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971549"
---
# <a name="using-makecert"></a>Utilisation de MakeCert

Les exemples suivants utilisent des commandes [Makecert](makecert.md) pour créer des certificats de test à l’aide des options disponibles avec Internet Explorer version 4,0 ou ultérieure.

-   Créez un certificat émis par la racine de test par défaut. Enregistrez le certificat dans un fichier.

    **Makecert** *MyNew. cer*

-   Créez un certificat émis par la racine de test par défaut. Enregistrez-le dans un magasin de certificats.

    **Makecert-SS** *MyNewStore*

-   Créez un certificat émis par la racine de test par défaut. Créez un conteneur de clé et enregistrez le certificat dans un magasin et un fichier.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*

-   Créez un certificat émis par la racine de test par défaut. Créez un fichier de clé privée et enregistrez le certificat dans un magasin et dans un fichier.

    **Makecert-SV** *MyKeyFile* **-SS** *MyNewStore* *MyNew. cer*

-   Créez un certificat émis par la racine de test par défaut. Créez un conteneur de clé, enregistrez le certificat dans un magasin et dans un fichier, puis rendez la clé privée exportable.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**

-   Créez un certificat à l’aide de la racine de test par défaut. Enregistrez le certificat dans un magasin. Créez ensuite un autre certificat émis par le certificat créé récemment. Enregistrez le deuxième certificat dans un autre magasin.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* **Makecert-is** *MyNewStore* **-SS** *AnotherStore*

-   Créez un certificat à l’aide de la racine de test par défaut. Enregistrez le certificat dans le magasin MY. Créez ensuite un autre certificat à l’aide du certificat créé récemment. S’il y a plus d’un certificat dans mon magasin, le certificat doit être identifié à l’aide de son nom commun.

    **Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS mon Makecert-est My-in "XXZZYY"-SS** *AnotherStore*

-   Créez un certificat à l’aide de la racine de test par défaut. Enregistrez le certificat dans mon magasin et dans un fichier. Créez ensuite un autre certificat à l’aide du certificat *MyNew* nouvellement créé. S’il existe plus d’un certificat dans mon magasin, identifiez le premier certificat de manière unique à l’aide du nom du fichier de certificat.

    **Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My** *MyNew. cer* **Makecert-is My-IC** *MyNew. cer* **-SS** *AnotherStore*

 

 



