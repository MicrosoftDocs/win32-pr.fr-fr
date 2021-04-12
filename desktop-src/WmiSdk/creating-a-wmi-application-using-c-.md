---
description: 'Pour créer une application pour WMI à l’aide de C++ : vous devez initialiser COM, accéder aux protocoles WMI et les définir, et effectuer un nettoyage manuel.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Création d’une application WMI à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320338"
---
# <a name="creating-a-wmi-application-using-c"></a>Création d’une application WMI à l’aide de C++

Pour créer une application pour WMI à l’aide de C++ : vous devez initialiser COM, accéder aux protocoles WMI et les définir, et effectuer un nettoyage manuel. Toutefois, C++ présente l’avantage de la flexibilité et de la puissance. Par conséquent, bien que vous soyez mieux servi à utiliser Visual Basic Scripting Edition (VBScript) ou Windows PowerShell pour des processus simples, C++ fonctionne mieux pour des applications plus sophistiquées et est nécessaire pour écrire des [fournisseurs](providing-data-to-wmi.md).

La procédure suivante décrit comment créer une application WMI.

**Pour créer une application WMI**

1.  [Initialisez com](initializing-com-for-a-wmi-application.md).

    Étant donné que WMI est basé sur la technologie COM, vous devez effectuer des appels aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour accéder à WMI.

2.  [Créer une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).

    Par définition, WMI s’exécute dans un processus différent de celui de votre application. Par conséquent, vous devez créer une connexion entre votre application et WMI.

3.  [Définissez les niveaux de sécurité sur la connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).

    Pour utiliser la connexion que vous créez à WMI, vous devez définir les niveaux d’emprunt d’identité et d’authentification pour votre application.

4.  Implémentez le rôle de votre application.

    WMI expose une variété d’interfaces COM qui permettent d’accéder aux données et de les manipuler au sein de votre entreprise. Pour plus d’informations, consultez [manipulation d’informations de classes et d’instances](manipulating-class-and-instance-information.md), [réception d’un événement WMI](receiving-a-wmi-event.md)et [de l’API com pour WMI](com-api-for-wmi.md).

    C’est là que la majeure partie de votre application cliente WMI doit exister, comme l’accès aux objets WMI ou la manipulation des données.

5.  [Nettoyez et arrêtez votre application](cleaning-up-and-shutting-down-a-wmi-application.md).

    Une fois que vous avez terminé vos requêtes dans WMI, vous devez détruire tous les pointeurs COM et arrêter correctement votre application.

Pour plus d’informations et pour obtenir un exemple de code sur la création d’une application WMI, consultez [exemple : création d’une application WMI](example-creating-a-wmi-application.md).

 

 
