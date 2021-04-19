---
description: La configuration des stratégies IPSec et des associations de sécurité pour IPv6 s’effectue avec Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515238"
---
# <a name="ipsec6exe"></a>Ipsec6.exe

La configuration des stratégies IPSec et des associations de sécurité pour IPv6 s’effectue avec Ipsec6.exe. Les Ipsec6.exe sous-commandes sont les suivantes :

<dl> <dt>

<span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**Ipsec6 SP \[** _Interface_*_\]_*
</dt> <dd>

Affiche les stratégies de sécurité actives. Vous pouvez également afficher des stratégies de sécurité actives pour une interface spécifique.

</dd> <dt>

<span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**Ipsec6 sa**
</dt> <dd>

Affiche les associations de sécurité actives.

</dd> <dt>

<span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 c \[** _Nom de fichier (sans extension)_*_\]_*
</dt> <dd>

Crée les fichiers utilisés pour configurer les associations de sécurité et de stratégie de sécurité. Crée *filename*. SPD pour les stratégies de sécurité et *nom de fichier*. sad pour les associations de sécurité. Utilisez les fichiers créés en tant que modèles pour configurer des stratégies de sécurité ou des associations de sécurité. Les fichiers peuvent être modifiés à l’aide d’un éditeur de texte. Pour appeler la configuration contenue dans les fichiers SPD et SAD, utilisez la commande **Ipsec6 a** .

</dd> <dt>

<span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 a \[** _Nom de fichier (sans extension)_*_\]_*
</dt> <dd>

Ajoute des stratégies de sécurité dans *filename*. SPD et des associations de sécurité dans *filename*. Sad à la liste des stratégies de sécurité et des associations de sécurité actives.

</dd> <dt>

<span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 i \[**  *_\] \[_* _Nom de fichier de stratégie (sans extension)_*_\]_*
</dt> <dd>

Ajoute des stratégies de sécurité dans *filename*. SPD et des associations de sécurité dans *filename*. Sad à la liste des stratégies de sécurité actives et des associations de sécurité, telles qu’elles sont référencées par le numéro de stratégie.

</dd> <dt>

<span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**Ipsec6 d \[ type = SP sa \] \[** _IndexNumber_*_\]_*
</dt> <dd>

Supprime les stratégies de sécurité ou les associations de sécurité de la liste des stratégies de sécurité actives et des associations de sécurité, telles qu’elles sont référencées par leur numéro d’index (affiché avec **Ipsec6 SP** ou **Ipsec6 sa**).

</dd> </dl>

 

 



