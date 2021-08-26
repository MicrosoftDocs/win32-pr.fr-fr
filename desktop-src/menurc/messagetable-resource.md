---
title: Ressource MESSAGETABLE
description: Définit l’ID et le fichier de la ressource de table de messages d’une application. Les tables de messages sont des ressources de chaîne spéciales utilisées dans la journalisation des événements et avec la fonction FormatMessage. Le fichier contient une table de messages binaires générée par le compilateur de message, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- Menus de ressources MESSAGETABLE et autres ressources
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378860e10ab6da929147e13a8120ee169204276e3c609b20176c22df9de15dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886719"
---
# <a name="messagetable-resource"></a>Ressource MESSAGETABLE

Définit l’ID et le fichier de la ressource de table de messages d’une application. Les tables de messages sont des ressources de chaîne spéciales utilisées dans la journalisation des événements et avec la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . Le fichier contient une table de messages binaires générée par le compilateur de message, MC.EXE.

Le compilateur de message génère également un fichier de script de ressources qui contient les instructions **MESSAGETABLE** dont vous avez besoin pour inclure les ressources de table de messages dans le fichier de ressources compilé. Utilisez la directive [**\# include**](-include.md) pour inclure ce script de ressources dans votre script de ressources principal.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits identifiant la ressource.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Nom du fichier qui contient la ressource. Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel.

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="examples"></a>Exemples

L’exemple suivant définit une ressource **MESSAGETABLE** :

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 