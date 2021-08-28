---
description: Les entrées suivantes dans les colonnes format, type et ContextData de la table ModuleConfiguration spécifient le type sémantique des informations qui sont remplacées dans l’élément configurable spécifié dans la colonne nom de cette table.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Types sémantiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234e5dd929991c2ec5fecbc1d2d1bda72f4fbe52
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882644"
---
# <a name="semantic-types"></a>Types sémantiques

Les entrées suivantes dans les colonnes format, type et ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md) spécifient le type sémantique des informations qui sont remplacées dans l’élément configurable spécifié dans la colonne nom de cette table.

[Types de format de texte](text-format-types.md)



| Format | Type       | ContextData                                                 | Description                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Texte   |            |                                                             | Texte arbitraire. Consultez [type de texte arbitraire](arbitrary-text-type.md).                                        |
| Texte   | Énumération       | <A>=<a>;<B>=<b>;&lt; C &gt; c = &lt;&gt; | Valeur sélectionnée dans un jeu. Consultez [type enum](enum-type.md).                                                 |
| Texte   | Mis en forme  |                                                             | Valeur qui répond à la définition du texte mis en forme dans le programme d’installation. Consultez [type mis en forme](formatted-type.md). |
| Texte   | RTF        |                                                             | Chaîne de texte RTF. Consultez [type RTF](rtf-type.md).                                                          |
| Texte   | Identificateur |                                                             | chaîne de texte conforme à un [identificateur](identifier.md)de Windows Installer.                              |



 

[Types de format d’entier](integer-format-types.md)



| Format  | Type | ContextData | Description                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Entier |      |             | Toute valeur entière. Consultez [type entier arbitraire](arbitrary-integer-type.md). |



 

[Types de format de clé](key-format-types.md)



| Format | Type      | ContextData      | Description                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Clé    | Fichier      | AssemblyContext  | Permet aux utilisateurs de configurer des clés étrangères sur des assemblys Win32 ou common language runtime. Consultez [type de fichier](file-type.md). |
| Clé :    | Binary    | Bitmap           | Clé étrangère vers une ligne de table binaire contenant une bitmap à utiliser dans l’interface utilisateur. Consultez [type binaire](binary-type.md).                  |
| Clé :    | Binary    | Icône             | Clé étrangère vers une ligne de table binaire contenant une icône à utiliser dans l’interface utilisateur. Consultez [type binaire](binary-type.md).                   |
| Clé :    | Binary    | EXE              | Clé étrangère vers une ligne de table binaire contenant un EXE 32 bits. Consultez [type binaire](binary-type.md).                             |
| Clé :    | Binary    | EXE64            | Clé étrangère vers une ligne de table binaire contenant un EXE 32 ou 64 bits. Consultez [type binaire](binary-type.md).                       |
| Clé :    | Icône      | ShortcutIcon     | Clé étrangère vers une ligne de table d’icônes contenant une icône pour une utilisation par un raccourci. Consultez [type d’icône](icon-type.md).                |
| Clé :    | Boîte de dialogue    | DialogNext       | Clé étrangère vers une ligne de la table de boîtes de dialogue. Consultez [type de dialogue](dialog-type.md).                                                 |
| Clé :    | Boîte de dialogue    | DialogPrev       | Clé étrangère vers une ligne de la table de boîtes de dialogue. Consultez [type de dialogue](dialog-type.md).                                                 |
| Clé :    | Répertoire | IsolationDir     | Clé étrangère vers une ligne de la table de répertoires à laquelle les fichiers isolés appartiennent. Consultez [type de répertoire](directory-type.md).            |
| Clé :    | Répertoire | ShortcutLocation | Clé étrangère vers une ligne de la table de répertoire dans laquelle un raccourci doit être installé. Consultez [type de répertoire](directory-type.md).   |
| Clé    | Propriété  |                  | Clé étrangère vers une ligne de propriété. Consultez [type de propriété](property-type.md).                                                 |
| Clé    | Propriété  | Public           | Clé étrangère vers une ligne de propriété. Consultez [type de propriété](property-type.md).                                                 |
| Clé    | Propriété  | Privées          | Clé étrangère vers une ligne de propriété. Consultez [type de propriété](property-type.md).                                                 |



 

[Types de format de champ de format binaire](bitfield-format-types.md)



| Format   | Type | ContextData                                  | Description                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Champ |      | &lt;Mask &gt; ; <A> = <a> ; <B> = b | Modifie un sous-ensemble de bits dans une colonne. Consultez [type de champ de binaire arbitraire](arbitrary-bitfield-type.md). |



 

 

 



