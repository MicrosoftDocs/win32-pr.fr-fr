---
title: Clés de registre COM
description: Clés de registre COM
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b85bb84b0a6f2e6ccc233b68af2889f4cb11ab
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363420"
---
# <a name="com-registry-keys"></a>Clés de registre COM

Le registre contient une multitude d’informations utilisées par COM. Les informations les plus importantes sont stockées dans les clés suivantes.



| Clé                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Regroupe les options de configuration (un ensemble de valeurs nommées) pour un ou plusieurs objets COM distribués dans un seul emplacement du Registre. Les sous-clés sous cette clé sont utilisées pour mapper un identificateur d’application (AppID) à un nom de serveur distant. Pour simplifier la gestion des paramètres de sécurité et de configuration courants, les objets COM distribués hébergés par le même exécutable sont regroupés en un seul AppID.<br/>                                                                                                                                                                                                                                                                                                                      |
| [IDENTIFICATEUR](clsid-key-hklm.md)<br/>                              | Un identificateur de classe (CLSID) est un identificateur global unique qui identifie un objet de classe COM. Si le serveur ou le conteneur autorise la liaison à des objets incorporés, inscrivez un CLSID pour chaque classe d’objets prise en charge. La clé CLSID contient les informations utilisées par le gestionnaire COM par défaut pour retourner les informations relatives à une classe lorsqu’elle est à l’État en cours d’exécution.<br/> pour obtenir un CLSID pour votre application, utilisez uuidgen.exe, situé dans le \\ répertoire TOOLs du Shared Computer Toolkit COM, ou utilisez [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Un identificateur programmatique (ProgID) est une entrée de Registre qui peut être associée à un CLSID. La clé ProgID mappe une chaîne conviviale à un CLSID. À l’instar du CLSID, le ProgID identifie une classe, mais avec une précision moindre. Utilisez un ProgID en programmation dans des situations où il n’est pas possible d’utiliser un CLSID. Les ProgID ne doivent pas apparaître dans l’interface utilisateur. Il n’est pas garanti que les ProgID soient uniques, donc ils ne peuvent être utilisés que lorsque des collisions de noms n’ont pas lieu.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Associe un ProgID à un CLSID. Il est utilisé pour déterminer la version la plus récente d’une application d’objet. À l’instar du ProgID, le ProgID indépendant de la version peut être inscrit avec un nom explicite. <br/> Les applications doivent inscrire un identificateur de programmation indépendant de la version sous la clé VersionIndependentProgID. Le ProgID indépendant de la version fait référence à la classe de l’application et ne passe pas de la version à la version, mais reste constante dans toutes les versions. Il est utilisé avec les langages de macro et fait référence à la version actuellement installée de la classe de l’application. Le ProgID indépendant de la version doit correspondre au nom de la version la plus récente de l’application objet. <br/> |
| [extension de fichier \_](-file-extension--key.md)<br/>              | Associe une extension de nom de fichier à un ProgID.<br/> Les informations contenues dans la clé d’extension de nom de fichier sont utilisées par les [monikers](file-monikers.md)système et de fichier. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) utilise la clé d’extension de nom de fichier pour fournir le CLSID associé. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interface](interface-key.md)<br/>                           | Inscrit les nouvelles interfaces en associant un nom d’interface à un identificateur d’interface (IID). Elle mappe des IID à des informations spécifiques à une interface. Les informations sont requises principalement pour l’utilisation d’interfaces au-delà des limites du processus. <br/> Lors de l’ajout d’une nouvelle interface, la clé de l’interface doit être complétée pour que COM inscrive la nouvelle interface. Il doit y avoir une sous-clé IID pour chaque nouvelle interface. <br/>                                                                                                                                                                                                                                                                                                       |
| [ActiveX](hkey-local-machine-software-microsoft-ole.md)<br/>     | Contrôle le lancement et les autorisations d’accès par défaut pour les objets COM distribués, ainsi que les fonctionnalités de sécurité au niveau des appels pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Seuls les administrateurs ont un accès complet à cette partie du Registre. Tous les autres utilisateurs disposent d’un accès en lecture seule. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des applications COM](registering-com-applications.md)
</dt> </dl>

 

 





