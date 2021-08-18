---
description: La liste suivante répertorie les meilleures pratiques recommandées pour l’utilisation des associations de fichiers.
title: Meilleures pratiques pour les associations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8cfa57faea9423af31e494c37d97af2b61d690095fb669a6a9b47109f6e97e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094214"
---
# <a name="best-practices-for-file-associations"></a>Meilleures pratiques pour les associations de fichiers

La liste suivante répertorie les meilleures pratiques recommandées pour l’utilisation des associations de fichiers.

-   [Ne pas copier les associations de fichiers à partir du Registre](#do-not-copy-file-associations-from-the-registry)
-   [Évitez les chemins d’accès Hard-Coding dans le registre, le cas échéant.](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Toujours encapsuler les chaînes de développement entre guillemets](#always-wrap-expanding-strings-in-quotation-marks)
-   [Ne confondez pas l’exécution automatique/la lecture automatique avec les associations de fichiers](#do-not-confuse-autoplayautorun-with-file-associations)
-   [Ne confondez pas la base de données MIME d’Internet Explorer avec les associations de fichiers](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Utiliser des ProgID correctement formés et avec version](#use-properly-formed-and-versioned-progids)
-   [Ne pas utiliser les extensions de nom de fichier courtes](#do-not-use-short-file-name-extensions)
-   [Inscrire de nouveaux types de fichiers dans la base de données MIME IANA](#register-new-file-types-in-the-iana-mime-database)
-   [s’inscrire auprès du Service Web Windows pour les Associations de fichiers](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Rubriques connexes](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>Ne pas copier les associations de fichiers à partir du Registre

Nous vous recommandons de ne pas copier les associations de fichiers existantes à partir du Registre. Cela provoque souvent la propagation d’associations de fichiers mal formés. Au lieu de cela, vous devez suivre les étapes décrites dans [scénario d’exemple d’association de fichiers](fa-sample-scenarios.md).

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Évitez les chemins d’accès Hard-Coding dans le registre, le cas échéant.

Tout comme les chemins d’accès codés en dur dans les programmes peuvent entraîner des problèmes, les chemins d’accès codés en dur dans le registre peuvent également entraîner des problèmes. Au lieu de cela, vous devez utiliser des chaînes d’expansion du Registre (REG \_ expand \_ SZ) pour fournir l’indépendance du chemin d’accès, le cas échéant. Par exemple, au lieu d’utiliser cette méthode :

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

Vous devez utiliser cette méthode :

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Toujours encapsuler les chaînes de développement entre guillemets

Le développement de chaînes peut contenir des espaces quand ils se développent. Étant donné que les espaces sont souvent interprétés comme des délimiteurs d’arguments, ils entraînent des problèmes dans certaines circonstances. Par exemple, une commande permettant d’appeler MyProgram peut être stockée dans le registre comme suit :

`%SYSTEMROOT%\MyProgram %1 %2`

MyProgram s’attend à ce que %1 soit le chemin d’accès complet à un nom de fichier et %2 un commutateur pour indiquer une action. Si cette commande est exécutée avec les arguments **C : \\ Program Files \\ My documents \\document.txt** et **/Print**, et en supposant que la racine du lecteur c : \\ WinNT, elle se développe en :

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

Dans ce cas, MyProgram interprète que le premier argument est C : \\ Program et le deuxième argument est Files \\ My, qui n’est pas le comportement prévu. Les arguments sont interprétés correctement, toutefois, qu’ils contiennent ou non des espaces, si les chaînes de développement sont encapsulées entre guillemets comme suit :

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>Ne confondez pas l’exécution automatique/la lecture automatique avec les associations de fichiers

Les associations de fichiers sont similaires à la lecture automatique/exécution automatique d’une certaine manière. Toutefois, l’exécution automatique/autorun offre des fonctionnalités distinctes et distinctes de celles fournies par les associations de fichiers. Pour plus d’informations, consultez [création d’une application de CD-ROM compatible avec l’exécution automatique](autoplay.md).

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>Ne confondez pas la base de données MIME d’Internet Explorer avec les associations de fichiers

les Associations de fichiers sont similaires à la Windows base de données MIME d’Internet Explorer, dans la mesure où les types de fichiers peuvent (et doivent) inclure une définition de type mime. Toutefois, la base de données MIME d’Internet Explorer est séparée et distincte des associations de fichiers.

## <a name="use-properly-formed-and-versioned-progids"></a>Utiliser des ProgID correctement formés et avec version

Utilisez toujours des [ProgID avec version](fa-progids.md), même s’il n’existe qu’une seule version du ProgID. Les ProgID avec version permettent d’éviter les conflits de ProgID et les remplacements. Ils permettent également aux différentes versions d’une application de coexister.

## <a name="do-not-use-short-file-name-extensions"></a>Ne pas utiliser les extensions de nom de fichier courtes

Les extensions de nom de fichier longues offrent les avantages suivants :

-   La longueur limitée des extensions courtes les rend vulnérables aux *collisions d’extension.* Une collision d’extension se produit lorsque la même extension est utilisée pour classer plusieurs types de fichiers. L’utilisation d’extensions longues réduit considérablement les risques de collision.
-   Les noms de fichiers courts tendent à être énigmatiques. Les extensions longues ont tendance à être plus significatives, car des informations supplémentaires peuvent être incorporées dans l’extension.

Pour plus d’informations, consultez [extensions de noms de fichiers](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Inscrire de nouveaux types de fichiers dans la base de données MIME IANA

L’IANA (Internet Assigned Numbers Authority) conserve une base de données publique de types MIME inscrits. Lors de la définition d’un nouveau type de fichier public, nous vous recommandons de définir également un type MIME pour le type de fichier et d’inscrire ce type auprès de l’IANA. L’inscription n’est pas coûteuse.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>s’inscrire auprès du Service Web Windows pour les Associations de fichiers

les développeurs d’applications peuvent s’inscrire auprès du Service Web Windows que les utilisateurs utilisent pour rechercher des applications pouvant fonctionner sur des types de fichiers spécifiques. le processus d’inscription au service web est détaillé dans [Windows processus d’intégration du système d’Association de fichiers](https://support.microsoft.com/kb/929149).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de scénario d’association de fichiers](fa-sample-scenarios.md)
</dt> <dt>

[instructions pour la gestion des Applications par défaut dans Windows Vista et versions ultérieures](vista-managing-defaults.md)
</dt> <dt>

[Programmes par défaut](default-programs.md)
</dt> <dt>

[Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



