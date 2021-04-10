---
description: Décrit le fichier de configuration WsdCodeGen.
ms.assetid: 6dc340db-221e-4389-ba76-9f189f91866b
title: Fichier de configuration WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8c252c5361fda411e2b7eca4f906ba92085a552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114835"
---
# <a name="wsdcodegen-configuration-file"></a>Fichier de configuration WsdCodeGen

Un fichier de configuration WsdCodeGen est généralement généré par l’outil WsdCodeGen. Vous pouvez créer des fichiers de configuration manuellement, mais la complexité et la longueur du fichier empêchent généralement le codage manuel. Nous vous recommandons fortement d’utiliser WsdCodeGen pour générer le fichier. Pour plus d’informations sur la génération de fichiers de configuration, consultez Utilisation de la [syntaxe de ligne de commande](wsdcodegen-command-line-syntax.md) [WsdCodeGen](using-wsdcodegen.md) et WsdCodeGen.

Vous devez examiner le fichier de configuration généré et, si nécessaire, le modifier avant de l’utiliser pour créer le code source. Le fichier de configuration généré par WsdCodeGen est généralement suffisant pour le développement de clients.

Pour utiliser le fichier de configuration pour le développement de serveur, certaines modifications sont nécessaires. Si l’hébergement est activé (par exemple, si le mode « tous » ou « hôte » est sélectionné), modifiez le contenu de l’élément [**ThisModelMetadata**](thismodelmetadata.md) et de ses éléments enfants si nécessaire. En outre, modifiez ou supprimez les éléments [**PnPXDeviceCategory**](/windows/desktop/WsdApi/pnpxdevicecategory), [**PnPXHardwareId**](pnpxhardwareid.md)et [**PnPXCompatibleId**](/windows/desktop/WsdApi/pnpxcompatibleid) à l’intérieur de l’élément **ThisModelMetadata** ou les éléments [**hébergés**](hosted.md) , si nécessaire.

Un fichier de configuration se compose d’une séquence d’éléments qui fournissent des données d’entrée pour la génération de code, suivi de n’importe quel nombre d’éléments de [**fichier**](file.md) qui décrivent les fichiers à générer. Les données d’entrée incluent quelques propriétés globales et des références à des types exprimés dans des assemblys WSDL, XSD et managés. Texte et CDATA dans les éléments de **fichier** sont écrits dans les fichiers générés sans modification. D’autres éléments dans les éléments de **fichier** sont remplacés dans les fichiers générés par le code généré.

Les fichiers de configuration XML doivent suivre quelques règles générales pour être correctement formatées pour être utilisées avec l’utilitaire de génération de code. Celles-ci sont les suivantes :

-   L’élément racine d’un fichier de configuration est [**wsdCodeGen**](wsdcodegen.md).

-   Les éléments qui contiennent des types de données simples sont interchangeables avec des attributs. Par exemple :

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    équivaut à :

    ``` syntax
    <wsdCodeGen layerNumber="1"/>
    ```

-   En général, il n’y a aucune contrainte sur l’ordre des éléments. Par exemple :

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
        <layerPrefix>MEDIA_</layerPrefix>
    </wsdCodeGen>
    ```

    équivaut à :

    ``` syntax
    <wsdCodeGen>
        <layerPrefix>MEDIA_</layerPrefix>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    Toutefois, le générateur de code traite le fichier de configuration en une seule passe, et le classement est pertinent. Par exemple, les éléments de [**fichier**](file.md) qui génèrent du code relatif à un type de port particulier doivent se produire après l’élément qui indique au générateur de code de lire le contrat de type de port.

Pour obtenir la liste complète des éléments utilisés dans les fichiers de configuration WsdCodeGen, consultez [référence XML du fichier de configuration WsdCodeGen](wsdcodegen-configuration-file-xml-reference.md).

Les exemples de fichiers de configuration sont fournis avec le SDK Windows. Pour plus d’informations, consultez [exemples wsdapi](wsdapi-samples.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WsdCodeGen](about-wsdcodegen.md)
</dt> <dt>

[Exemples WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 
