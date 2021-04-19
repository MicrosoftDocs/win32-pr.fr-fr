---
description: La table de classe contient des informations relatives au serveur COM qui doivent être générées dans le cadre de la publication du produit. Chaque ligne peut générer un ensemble de clés et de valeurs de registre. Les informations ProgId associées sont incluses dans ce tableau.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Table de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520525"
---
# <a name="class-table"></a>Table de classe

La table de classe contient des informations relatives au serveur COM qui doivent être générées dans le cadre de la publication du produit. Chaque ligne peut générer un ensemble de clés et de valeurs de registre. Les informations ProgId associées sont incluses dans ce tableau.

La table de classe contient les colonnes suivantes.



| Colonne           | Type                         | Clé | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | O   | N        |
| Context          | [Identificateur](identifier.md) | O   | N        |
| -\_      | [Identificateur](identifier.md) | O   | N        |
| ProgId \_ par défaut  | [Text](text.md)             | N   | O        |
| Description      | [Text](text.md)             | N   | O        |
| AppId\_          | [GUID](guid.md)             | N   | O        |
| FileTypeMask     | [Text](text.md)             | N   | O        |
| Icône\_           | [Identificateur](identifier.md) | N   | O        |
| IndexIcône        | [Integer](integer.md)       | N   | O        |
| DefInprocHandler | [Nom du fichier](filename.md)     | N   | O        |
| Argument         | [Correct](formatted.md)   | N   | O        |
| Fonctionnalité\_        | [Identificateur](identifier.md) | N   | N        |
| Attributs       | [Integer](integer.md)       | N   | O        |



 

## <a name="column-information"></a>Informations sur les colonnes

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>IDENTIFICATEUR
</dt> <dd>

Identificateur de classe (ID) d’un serveur COM.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contexte
</dt> <dd>

Contexte de serveur pour ce serveur. Entrez l’une des valeurs suivantes pour la clé CLSID.



| CLÉ CLSID                             | Description                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Spécifie le chemin d’accès complet à une application serveur locale 16 bits.             |
| [LocalServer32](../com/localserver32.md)   | Spécifie le chemin d’accès complet à une application serveur locale 32 bits.             |
| [InprocServer](../com/inprocserver.md)     | Spécifie le chemin d’accès à une DLL de serveur in-process.                           |
| [InprocServer32](../com/inprocserver32.md) | Spécifie le chemin d’accès à un serveur in-process 32 bits et le modèle de thread. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la [table de composants](component-table.md) spécifiant le composant dont le fichier de clé fournit le serveur com.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ par défaut
</dt> <dd>

ID de programme par défaut associé à cet ID de classe. Cette colonne est une clé étrangère dans la [table ProgID](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description localisée associée à l’ID de classe et à l’ID de programme.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_
</dt> <dd>

ID d’application contenant les informations DCOM pour l’application associée ( [GUID](guid.md)de chaîne). Cette colonne est une clé étrangère dans la [table AppID](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Contient des informations pour la clé HKCR (ce CLSID).

Si plusieurs modèles existent, ils doivent être délimités par un point-virgule et les sous-clés numériques sont générées : 0, 1, 2... Pour plus d’informations sur cette fonctionnalité, consultez [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Située\_
</dt> <dd>

Fichier fournissant l’icône associée à ce CLSID. Le programme d’installation écrit l’entrée dans cette colonne sous la clé DefaultIcon associée au ProgId. Si la valeur n’est pas null, la colonne est une clé étrangère dans la [table d’icônes](icon-table.md). Si la valeur est null, le serveur COM fournit la ressource icône. Les associations et les raccourcis de fichiers publiés requièrent une valeur non null dans cette colonne pour s’afficher correctement.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IndexIcône
</dt> <dd>

Index d’icône dans le fichier d’icône. Peut être Null.

Nombres non négatifs uniquement.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Ce champ spécifie le gestionnaire in-process par défaut pour le contexte de serveur spécifié dans le champ de contexte.

Ce champ doit avoir la valeur null si une clé de CLSID InprocServer ou InprocServer apparaît dans le champ de contexte.

Si une clé de CLSID LocalServer ou LocalServer32 apparaît dans le champ de contexte, la valeur du champ DefInprocHandler identifie le gestionnaire in-process par défaut.



| Valeur                | Description                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valeur non numérique    | Le programme d’installation traite une valeur non numérique dans le champ DefInprocHandler comme un fichier système servant de gestionnaire in-process 32 bits spécifié par la clé InprocHandler32.                                                                                                            |
| Null                 | Les champs DefInprocHandler et argument peuvent tous deux avoir la valeur null pour une clé de CLSID LocalServer ou LocalServer32.                                                                                                                                                                           |
| 1 = par défaut (système) | La valeur par défaut est le gestionnaire in-process 16 bits spécifié par InprocHandler. Dans ce cas, la valeur de InprocHandler est le nom dans le Registre sous lequel la valeur du gestionnaire in-process par défaut est stockée. Par exemple, HKEY \_ local \_ machine machine \\ Software \\ classes \\ CLSID.     |
| 2 = par défaut (système) | La valeur par défaut est le gestionnaire in-process 32 bits spécifié par InprocHandler32. Dans ce cas, la valeur de InprocHandler32 est le nom dans le Registre sous lequel la valeur du gestionnaire in-process par défaut est stockée. Par exemple, HKEY \_ local \_ machine machine \\ Software \\ classes \\ CLSID. |
| 3 = valeur par défaut (système) | La valeur par défaut est un gestionnaire in-process 16 bits ou 32 bits.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Si une clé de CLSID LocalServer ou LocalServer32 apparaît dans le champ de contexte, le texte de ce champ est enregistré en tant qu’argument sur le serveur et est utilisé par COM pour appeler le serveur. Les champs DefInprocHandler et argument peuvent tous les deux avoir la valeur null si LocalServer ou LocalServer32 apparaît dans le champ de contexte.

Notez que la résolution des propriétés dans le champ argument est limitée. Une propriété mise en forme en tant que \[ propriété \] dans ce champ ne peut être résolue que si la propriété a déjà la valeur prévue lorsque le composant propriétaire de la classe est installé. Par exemple, pour que l’argument « \[ \#MyDoc.doc\] » soit résolu à la valeur correcte, le même processus doit installer le fichier MyDoc.doc et le composant qui possède la classe.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Clé externe dans la [table de fonctionnalités](feature-table.md) spécifiant la fonctionnalité qui fournit le serveur com.

Clé externe vers la colonne de l’une des tables de fonctionnalités.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Si **msidbClassAttributesRelativePath** est défini dans cette colonne, le nom de fichier complet peut être utilisé pour les serveurs com. Le programme d’installation enregistre le nom de fichier uniquement au lieu du chemin d’accès complet. Cela permet au serveur dans le répertoire actif de prendre la priorité et autorise plusieurs copies du même composant.



| Attribut                            | Decimal | Valeur hexadécimale |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est référencée lorsque l’action [RegisterClassInfo](registerclassinfo-action.md) ou l' [action UnregisterClassInfo](unregisterclassinfo-action.md) sont exécutées.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
