---
title: Fichiers générés pour une interface COM
description: Pour les interfaces COM, le compilateur MIDL combine toutes les données et routines auxiliaires du serveur d’objets et du client en un seul fichier proxy d’interface.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- Compilateur MIDL MIDL, MIDL et COM
- MIDL COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940915"
---
# <a name="files-generated-for-a-com-interface"></a>Fichiers générés pour une interface COM

Pour les interfaces COM, le compilateur MIDL combine toutes les données et routines auxiliaires du serveur d’objets et du client en un seul fichier proxy d’interface. Ce fichier comprend des points d’entrée de substitution pour les clients et les serveurs. En outre, le compilateur MIDL génère un fichier d’en-tête d’interface, un fichier UUID d’interface et un fichier d’inscription d’interface. Vous allez utiliser tous ces fichiers lors de la création d’une DLL de proxy qui contient le code pour prendre en charge l’utilisation de l’interface par les applications clientes et les serveurs d’objets. Vous allez également utiliser le fichier d’en-tête d’interface et le fichier UUID de l’interface lors de la création du fichier exécutable pour une application cliente qui utilise l’interface.

Les rubriques suivantes décrivent chacun des fichiers générés pour une interface COM personnalisée, que vous identifiez en incluant l’attribut d' **\[** [**objet**](object.md) **\]** dans la liste des attributs d’interface du fichier IDL :

-   [Fichier de proxy d’interface](the-interface-proxy-file.md)
-   [Fichiers d’en-tête](the-header-files.md)
-   [Fichier UUID de l’interface](the-interface-uuid-file.md)
-   [Fichier d’inscription de l’interface](the-interface-registration-file.md)

Pour plus d’informations, consultez [fichier de configuration d’application (ACF)](application-configuration-file-acf-.md), [**\_ configuration/App**](-app-config.md), [fichier de définition d’interface (IDL)](interface-definition-idl-file.md)et [génération et inscription d’une dll proxy](../com/building-and-registering-a-proxy-dll.md).

 

 