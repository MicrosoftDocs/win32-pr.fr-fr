---
title: Windows Glossaire du système de fichiers projeté
description: Termes spéciaux utilisés dans ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 12b6e90d98fce3882aa5dc8d552f88e9cd9f389d24673fdc5caf175e180082f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030981"
---
# <a name="windows-projected-file-system-glossary"></a>Windows Glossaire du système de fichiers projeté

Termes spéciaux utilisés dans ProjFS.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**magasin de stockage**
</dt>
<dd>

Données hiérarchiques gérées par le fournisseur et projetées dans le système de fichiers sous forme de fichiers et de répertoires.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**espace réservé de modification**
</dt>
<dd>

Fichier ou répertoire modifié localement et n’est plus un cache de son état dans le magasin du fournisseur.  Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**fichier/répertoire complet**
</dt>
<dd>

Un fichier ou un répertoire qui a été créé dans le système de fichiers local, ou un fichier qui a été modifié, ce qui n’est plus un cache de son état dans le magasin de stockage.  Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**espace réservé hydraté**
</dt>
<dd>

Fichier dont le contenu et les métadonnées ont été mis en cache sur le disque.  Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Situé**
</dt>
<dd>

Fichier ou répertoire qui n’est pas entièrement présent sur le disque.  Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**objet tombstone**
</dt>
<dd>

Espace réservé masqué spécial qui représente un élément qui a été supprimé du système de fichiers local.  Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**fichier/répertoire virtuel**
</dt>
<dd>

Fichier ou répertoire qui n’existe pas physiquement sur le disque, mais qui est projeté dans les résultats de l’énumération.  Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**instance de virtualisation**
</dt>
<dd>

Objet en mémoire qui gère la communication entre le fournisseur et ProjFS pour l’ensemble des fichiers et répertoires situés sous une racine de virtualisation particulière.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**racine de virtualisation**
</dt>
<dd>

Répertoire dans le système de fichiers sous lequel les données du fournisseur sont projetées.
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->