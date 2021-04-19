---
description: Considérations relatives à la création ou à l’ouverture d’un fichier à l’aide de la fonction CreateFile.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Création et ouverture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1430675862b10f9e9221d968242481525dc7632f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523365"
---
# <a name="creating-and-opening-files"></a>Création et ouverture de fichiers

La fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) peut créer un nouveau fichier ou ouvrir un fichier existant. Vous devez spécifier le nom de fichier, les instructions de création et d’autres attributs. Lorsqu’une application crée un nouveau fichier, le système d’exploitation l’ajoute au répertoire spécifié.

Le système d’exploitation attribue un identificateur unique, appelé *descripteur*, à chaque fichier ouvert ou créé à l’aide de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Une application peut utiliser ce handle avec les fonctions qui lisent, écrivent et décrivent le fichier. Elle est valide jusqu’à ce que toutes les références à ce handle soient fermées. Lorsqu’une application démarre, elle hérite de tous les descripteurs ouverts du processus qui l’a démarrée si les handles ont été créés comme pouvant être hérités.

Une application doit vérifier la valeur du handle retourné par [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avant de tenter d’utiliser le handle pour accéder au fichier. Si une erreur se produit, la valeur de handle est une **\_ \_ valeur de handle non valide** et l’application peut utiliser la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir des informations d’erreur étendues.

Quand une application utilise [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), elle doit utiliser le paramètre *dwDesiredAccess* pour spécifier si elle envisage de lire à partir du fichier, d’écrire dans le fichier, à la fois en lecture et en écriture, ou aucune des deux. C’est ce que l’on appelle demander un *mode d’accès*. L’application doit également utiliser le paramètre *dwCreationDisposition* pour spécifier l’action à effectuer si le fichier existe déjà, appelé disposition de *création*. Par exemple, une application peut appeler **CreateFile** avec *DwCreationDisposition* défini sur **Create \_ Always** pour toujours créer un nouveau fichier, même si un fichier du même nom existe déjà (remplaçant ainsi le fichier existant). Le fait que cette opération aboutisse ou non dépend de facteurs tels que les attributs et les paramètres de sécurité du fichier précédent (pour plus d’informations, consultez les sections suivantes).

Une application utilise également [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour spécifier si elle souhaite partager le fichier pour la lecture, l’écriture, les deux ou aucune des deux. C’est ce que l’on appelle le *mode de partage*. Un fichier ouvert qui n’est pas partagé (*dwShareMode* défini à zéro) ne peut pas être ouvert à nouveau, soit par l’application qui l’a ouvert, soit par une autre application, jusqu’à ce qu’il soit fermé. On parle également d’accès exclusif.

Lorsqu’un processus utilise [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour tenter d’ouvrir un fichier qui a déjà été ouvert en mode de partage (*dwShareMode* défini sur une valeur différente de zéro valide), le système compare les modes d’accès et de partage demandés à ceux spécifiés lors de l’ouverture du fichier. Si vous spécifiez un mode d’accès ou de partage qui entre en conflit avec les modes spécifiés dans l’appel précédent, **CreateFile** échoue.

Le tableau suivant illustre les combinaisons valides de deux appels à [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) à l’aide de différents modes d’accès et modes de partage (*dwDesiredAccess*, *dwShareMode* , respectivement). L’ordre dans lequel les appels **CreateFile** sont effectués n’a pas d’importance. Toutefois, toute opération d’e/s de fichier ultérieure sur chaque descripteur de fichier est toujours concédée par les modes d’accès et de partage actuels associés à ce descripteur de fichier particulier.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Premier appel à <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
<th>Appels de seconde valides à <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

En plus des attributs de fichier standard, vous pouvez également spécifier des attributs de sécurité en incluant un pointeur vers une structure d' [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) en tant que quatrième paramètre de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Toutefois, le système de fichiers sous-jacent doit prendre en charge la sécurité pour que cela ait un effet (par exemple, le système de fichiers NTFS le prend en charge, mais pas les différents systèmes de fichiers FAT). Pour plus d’informations sur les attributs de sécurité, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).

Une application qui crée un nouveau fichier peut fournir un handle facultatif à un fichier de modèle, à partir duquel [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) prend des attributs de fichier et des attributs étendus pour la création du nouveau fichier.

## <a name="createfile-scenarios"></a>Scénarios CreateFile

Il existe plusieurs scénarios fondamentaux pour initier l’accès à un fichier à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Ils sont résumés comme suit :

-   Création d’un nouveau fichier lorsqu’un fichier portant ce nom n’existe pas déjà.
-   La création d’un fichier même si un fichier du même nom existe déjà, l’effacement de ses données et le démarrage d’un fichier vide.
-   Ouverture d’un fichier existant uniquement s’il existe et uniquement intact.
-   Ouvrir un fichier existant uniquement s’il existe, le tronquer pour qu’il soit vide.
-   L’ouverture d’un fichier est toujours : telle quelle, si elle existe, en créant une nouvelle si elle n’existe pas.

Ces scénarios sont contrôlés par l’utilisation correcte du paramètre *dwCreationDisposition* . Vous trouverez ci-dessous une description de la façon dont ces scénarios correspondent aux valeurs de ce paramètre et à ce qui se passe quand elles sont utilisées.

Lors de la création ou de l’ouverture d’un nouveau fichier lorsqu’un fichier portant ce nom n’existe pas déjà (*dwCreationDisposition* défini sur **Create \_ New**, **Create \_ Always** ou **Open \_ Always**), la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) effectue les actions suivantes :

-   Combine les attributs de fichier et les indicateurs spécifiés par *dwFlagsAndAttributes* avec l' **Archive d' \_ attribut \_ de fichier**.
-   Définit la longueur du fichier sur zéro.
-   Copie les attributs étendus fournis par le fichier de modèle dans le nouveau fichier si le paramètre *hTemplateFile* est spécifié (cette valeur remplace tous les indicateurs **\_ attribut \_ \* de fichier* spécifiés précédemment).
-   Définit l’indicateur d’héritage spécifié par le membre _ *bInheritHandle** et le descripteur de sécurité spécifié par le membre **LpSecurityDescriptor** du paramètre *lpSecurityAttributes* (structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), s’il est fourni.

Lorsque vous créez un fichier même si un fichier du même nom existe déjà (*dwCreationDisposition* défini sur **Create \_ Always**), la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) effectue les actions suivantes :

-   Vérifie les attributs de fichier et les paramètres de sécurité actuels pour l’accès en écriture, échec en cas de refus.
-   Combine les attributs de fichier et les indicateurs spécifiés par *dwFlagsAndAttributes* avec l' **Archive d' \_ attribut \_ de fichier** et les attributs de fichier existants.
-   Définit la longueur du fichier sur zéro (autrement dit, toutes les données qui se trouvaient dans le fichier ne sont plus disponibles et le fichier est vide).
-   Copie les attributs étendus fournis par le fichier de modèle dans le nouveau fichier si le paramètre *hTemplateFile* est spécifié (cette valeur remplace tous les indicateurs **\_ attribut \_ \* de fichier* spécifiés précédemment).
-   Définit l’indicateur d’héritage spécifié par le membre _ *bInheritHandle** du paramètre *lpSecurityAttributes* (structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), s’il est fourni, mais ignore le membre **lpSecurityDescriptor** de la structure des **\_ attributs de sécurité** .
-   En cas de réussite (autrement dit, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) retourne un handle valide), l’appel de [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) produira **déjà l’erreur de code \_ \_**, bien que pour cette utilisation particulière, il ne s’agit pas réellement d’une erreur comme telle (si vous aviez l’intention de créer un fichier « nouveau » (vide) à la place de celui existant).

Lors de l’ouverture d’un fichier existant (*dwCreationDisposition* défini sur **Open \_ existing**, **Open \_ Always** ou **TRUNCATE \_ existing**), la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) effectue les actions suivantes :

-   Vérifie les attributs de fichier et les paramètres de sécurité actuels pour l’accès demandé, échec en cas de refus.
-   Combine les indicateurs de fichier (**\_ indicateur \_ \* de fichier* _) spécifiés par _dwFlagsAndAttributes * avec les attributs de fichier existants, et ignore tous les attributs de fichier (* * \_ attribut \_ \* de fichier* _) spécifiés par _dwFlagsAndAttributes *.
-   Définit la longueur du fichier sur zéro uniquement si *dwCreationDisposition* est défini sur **TRUNCATE \_ existing**, sinon la longueur du fichier actuel est conservée et le fichier est ouvert tel quel.
-   Ignore le paramètre *hTemplateFile* .
-   Définit l’indicateur d’héritage spécifié par le membre **bInheritHandle** du paramètre *lpSecurityAttributes* (structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), s’il est fourni, mais ignore le membre **lpSecurityDescriptor** de la structure des **\_ attributs de sécurité** .

## <a name="file-attributes-and-directories"></a>Attributs et répertoires de fichiers

Les attributs de fichier font partie des métadonnées associées à un fichier ou à un répertoire, chacun avec son objectif et des règles sur la façon dont il peut être défini et modifié. Certains de ces attributs s’appliquent uniquement aux fichiers, et à d’autres uniquement aux répertoires. Par exemple, l’attribut de **\_ \_ répertoire** de l’attribut de fichier s’applique uniquement aux répertoires : il est utilisé par le système de fichiers pour déterminer si un objet sur le disque est un répertoire, mais il ne peut pas être modifié pour un objet de système de fichiers existant.

Certains attributs de fichier peuvent être définis pour un répertoire, mais uniquement pour les fichiers créés dans ce répertoire, agissant comme des attributs par défaut. Par exemple, **l' \_ attribut \_ de fichier compressé** peut être défini sur un objet d’annuaire, mais étant donné que l’objet d’annuaire lui-même ne contient pas de données réelles, il n’est pas véritablement compressé ; Toutefois, les répertoires marqués avec cet attribut indiquent au système de fichiers de compresser les nouveaux fichiers ajoutés à ce répertoire. Tout attribut de fichier qui peut être défini sur un répertoire et qui sera également défini pour les nouveaux fichiers ajoutés à ce répertoire est appelé *attribut hérité*.

La fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) fournit un paramètre pour définir certains attributs de fichier lors de la création d’un fichier. En règle générale, ces attributs sont les plus courants qu’une application utilise au moment de la création du fichier, mais tous les attributs de fichier possibles ne sont pas disponibles pour **CreateFile**. Certains attributs de fichier requièrent l’utilisation d’autres fonctions, telles que [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa), [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)ou [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) , une fois que le fichier existe déjà. Dans le cas du **\_ \_ Répertoire des attributs de fichier**, la fonction [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) est nécessaire au moment de la création, car **CreateFile** ne peut pas créer de répertoires. Les autres attributs de fichier qui nécessitent un traitement spécial sont les fichiers de point d’analyse d’attribut de fichier et de fichier **\_ \_ partiellement alloué \_**, qui requièrent **DeviceIoControl**. **\_ \_ \_** Pour plus d’informations, consultez [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Comme indiqué précédemment, l’héritage d’attribut de fichier se produit lorsqu’un fichier est créé avec des attributs de fichier lus à partir des attributs d’annuaire où le fichier se trouvera. Le tableau suivant récapitule ces attributs hérités et leur relation avec les fonctionnalités [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .



| État de l’attribut d’annuaire                                      | Fonctionnalité de remplacement de l’héritage [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour les nouveaux fichiers      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Fichier \_ Jeu \_ compressé d’attribut** .<br/>                | Aucun contrôle. Utilisez [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) pour effacer.<br/>    |
| **Fichier \_ ATTRIBUT \_ compressé** non défini.<br/>            | Aucun contrôle. Utilisez [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) pour définir.<br/>      |
| **Fichier \_ Jeu \_ chiffré** de l’attribut.<br/>                 | Aucun contrôle. Utilisez [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **Fichier \_ ATTRIBUT \_ chiffré** non défini.<br/>             | Peut être défini à l’aide de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).<br/>                       |
| **Fichier \_ ATTRIBUT \_ not \_ Content \_ indexé** Set.<br/>     | Aucun contrôle. Utilisez [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) pour effacer.<br/> |
| **Fichier \_ ATTRIBUT \_ non \_ Content \_ indexé** non défini.<br/> | Aucun contrôle. Utilisez [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) pour définir.<br/>   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’accès](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Constantes d’attribut de fichier**](file-attribute-constants.md)
</dt> <dt>

[Compression et décompression de fichiers](file-compression-and-decompression.md)
</dt> <dt>

[Chiffrement de fichier](file-encryption.md)
</dt> <dt>

[Fonctions de gestion de fichiers](file-management-functions.md)
</dt> <dt>

[Handles et objets](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Gérer l’héritage](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Ouverture d’un fichier pour la lecture ou l’écriture](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

