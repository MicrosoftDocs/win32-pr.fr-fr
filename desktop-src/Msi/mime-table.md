---
description: La table MIME associe un type de contenu MIME à une extension de nom de fichier ou un CLSID pour générer l’extension ou les informations de serveur COM requises pour la publication du contenu MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Table MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e8a8f83499e286b63bf24dffa8858329231e74eec1f641588230da51578007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913369"
---
# <a name="mime-table"></a>Table MIME

La table MIME associe un type de contenu MIME à une extension de nom de fichier ou un CLSID pour générer l’extension ou les informations de serveur COM requises pour la publication du contenu MIME (Multipurpose Internet Mail Extensions).

La table MIME contient les colonnes suivantes.



| Colonne      | Type             | Clé | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | O   | N        |
| Extension\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>Indiquez
</dt> <dd>

Cette colonne est un identificateur pour le contenu MIME. Il est généralement écrit sous la forme d’un type/format.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Poste\_
</dt> <dd>

Cette colonne contient l’extension de serveur qui doit être associée au contenu MIME, sans le point. Cette colonne est une clé étrangère dans la [table d’extension](extension-table.md). La table d’extension contient des informations sur le serveur d’extension de nom de fichier utilisées dans le cadre de la publication.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>IDENTIFICATEUR
</dt> <dd>

Cette colonne contient le CLSID du serveur COM qui doit être associé au contenu MIME. Le CLSID de cette colonne peut être une clé étrangère dans la [table de classe](class-table.md) ou il peut s’agir d’un CLSID qui existe déjà sur l’ordinateur de l’utilisateur. La table de classe contient des informations relatives au serveur COM, qui sont utilisées dans le cadre de la publication.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette table est référencée lorsque l' [action RegisterMIMEInfo](registermimeinfo-action.md) ou l' [action UnregisterMIMEInfo](unregistermimeinfo-action.md) est exécutée. En mode publication, l’action RegisterMIMEInfo enregistre toutes les informations MIME pour les serveurs à partir de la table MIME pour laquelle la fonctionnalité correspondante est activée. Dans le cas contraire, l’action enregistre les informations MIME pour les serveurs de la table MIME pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être installée. L' [action UnregisterMIMEInfo](unregistermimeinfo-action.md) annule l’enregistrement des informations de Registre liées à MIME à partir du système. L’action annule l’enregistrement des informations MIME pour les serveurs de la table MIME pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



