---
title: La propriété informations de résumé définie
description: COM définit un jeu de propriétés communes standard pour le stockage des informations de synthèse sur les documents.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54f942d0c7f6c7d1ebc37feda80d55420ea6c8aaf896f4df15df2a5b7e7c0ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886825"
---
# <a name="the-summary-information-property-set"></a>La propriété informations de résumé définie

COM définit un jeu de propriétés communes standard pour le stockage des informations de synthèse sur les documents. Le jeu de propriétés d’informations de résumé doit être stocké dans un objet de flux. Autrement dit, ce jeu de propriétés doit être stocké en tant que jeu de propriétés simple. pour plus d’informations, consultez [Stockage et objets de flux pour un jeu de propriétés](storage-vs--stream-for-a-property-set.md).

Par exemple, pour créer un jeu de propriétés ANSI simple, vous devez appeler [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) pour créer le jeu de propriétés, en spécifiant **PROPSETFLAG \_ ANSI** (simple est le type de propriété par défaut), puis écrire dessus à l’aide d’un appel à [**IPropertyStorage :: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Pour lire le jeu de propriétés, vous devez appeler [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple).

Tous les jeux de propriétés partagées sont identifiés par un nom de flux ou de stockage avec le préfixe « \\ 005 » (ou 0x05) pour indiquer qu’il s’agit d’un jeu de propriétés qui peut être partagé entre les applications. La propriété informations de résumé définie n’est pas une exception. Le nom du flux qui contient le jeu de propriétés d’informations de résumé est : **« \\ 005SummaryInformation »**

Il n’est pas nécessaire de connaître le nom de flux de la propriété définie lors de l’accès au moyen des méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ; dans ce cas, seul l’identificateur de format (FMTID) doit être connu. Le FMTID pour le jeu de propriétés d’informations de résumé est : **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

La déclaration de cette valeur est disponible dans le fichier d’en-tête en tant que **fmtid \_ SummaryInformation**. Pour plus d’informations, consultez les FMTIDS dans les [identificateurs de format du jeu de propriétés prédéfinis](predefined-property-set-format-identifiers.md).

Le tableau suivant répertorie les noms de propriété de type chaîne pour le jeu de propriétés d’informations de résumé, ainsi que les identificateurs de propriété et les indicateurs de type variable (VT) respectifs. Les noms ne sont généralement pas stockés dans le jeu de propriétés, mais sont déduits de la valeur de l’ID de propriété. Les entrées de la chaîne d’ID de propriété indiquées ici correspondent aux définitions trouvées dans les fichiers d’en-tête.

| Nom | Chaîne d’ID de propriété | ID de propriété | Type VT |
|------|--------------------|-------------|---------|
| Titre | \_titre PIDSI | 0x00000002 | VT- \_ LPSTR  |
| Objet | PIDSI \_ objet | 0x00000003 | VT- \_ LPSTR |
| Auteur | \_auteur PIDSI | 0x00000004 | VT- \_ LPSTR |
| Mots clés | \_Mots clés PIDSI | 0x00000005 | VT- \_ LPSTR |
| Commentaires | \_Commentaires PIDSI | 0x00000006 | VT- \_ LPSTR |
| Modèle | \_modèle PIDSI | 0x00000007 | VT- \_ LPSTR |
| Dernier enregistrement par | PIDSI \_ LASTAUTHOR | 0x00000008 | VT- \_ LPSTR |
| Revision Number | PIDSI \_ REVNUMBER | 0x00000009 | VT- \_ LPSTR |
| Heure de modification totale | PIDSI \_ edittime | Stop | VT \_ FILETIME (UTC) |
| Dernière impression | PIDSI \_ LASTPRINTED | 0x0000000B | VT \_ FILETIME (UTC) |
| Créer une heure/date (voir la remarque ci-dessous) | PIDSI \_ créer \_ DTM | 0x0000000C | VT \_ FILETIME (UTC) |
| Heure/date du dernier enregistrement (voir la remarque ci-dessous) | PIDSI \_ LASTSAVE \_ DTM | 0x0000000D | VT \_ FILETIME (UTC) |
| Nombre de pages | PIDSI \_ PageCount | 0x0000000E | VT \_ |
| Nombre de mots | PIDSI \_ WORDCOUNT | 0x0000000F | VT \_ |
| Nombre de caractères | PIDSI \_ charCount | 0x00000010 | VT \_ |
| Thumbnail | \_miniature PIDSI | 0x00000011 | \_CF VT |
| Nom de la création de l’application | PIDSI \_ appname | 0x00000012 | VT- \_ LPSTR |
| Sécurité | \_sécurité PIDSI | 0x00000013 | VT \_ |

> [!NOTE]
> Pour **créer** l’heure/date et l' **heure/la date du dernier enregistrement**, certaines méthodes de transfert de fichiers, telles qu’un téléchargement à partir d’un BBS, ne maintiennent pas correctement la version du système de fichiers de ces informations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Implémentation du jeu de propriétés d’informations de résumé](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




