---
description: Les clés de Registre peuvent être écrites dans le registre système une fois que tous les composants sélectionnés et leurs fichiers associés ont été installés.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modification du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230243"
---
# <a name="modifying-the-registry"></a>Modification du Registre

Les clés de Registre peuvent être écrites dans le registre système une fois que tous les composants sélectionnés et leurs fichiers associés ont été installés. Les actions standard liées à la modification du Registre doivent être séquencées après les actions standard d’installation de fichier, car les clés de registre ne peuvent pas être écrites, sauf si le composant et le fichier correspondants ont été correctement installés.

L' [action RegisterClassInfo](registerclassinfo-action.md) accède à la [table de classe](class-table.md) pour enregistrer les informations de classe com des composants installés.

L' [action RegisterExtensionInfo](registerextensioninfo-action.md) interroge la table d' [extension](extension-table.md) et la [table de verbes](verb-table.md) et enregistre les extensions et les informations de verbe de commande correspondantes auprès du système d’exploitation.

L' [action RegisterProgIdInfo](registerprogidinfo-action.md) gère l’inscription des informations ProgID OLE avec le système d’exploitation.

L' [action RegisterMIMEInfo](registermimeinfo-action.md) traite la [table MIME](mime-table.md) pour inscrire l’association entre un type de contexte MIME, l’extension de nom de fichier et le CLSID.

L' [action WriteRegistryValues](writeregistryvalues-action.md) traite la [table du registre](registry-table.md) et écrit les clés pour tous les composants qui ont été installés localement ou pour s’exécuter à partir de la source. La table de registre permet d’écrire des clés dans les ruches **\_ \_ racine de la classe HKEY**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ machine** et **HKEY \_ Users** .

L' [action RemoveRegistryValues](removeregistryvalues-action.md) supprime les clés qui ont été marquées pour être supprimées dans la colonne Name de la [table Registry](registry-table.md) ou de la [table RemoveRegistry](removeregistry-table.md).

L' [action RegisterTypeLibraries](registertypelibraries-action.md) traite la [table Typelib](typelib-table.md) et enregistre les bibliothèques de types installées avec le système.

 

 



