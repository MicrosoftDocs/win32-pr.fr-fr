---
description: Les \_ constantes d’indicateur de bit LINEMEDIACONTROL décrivent un ensemble d’opérations génériques sur les flux de média.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Constantes LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526796"
---
# <a name="linemediacontrol_-constants"></a>\_Constantes LINEMEDIACONTROL

Les constantes d’indicateur de bit **LINEMEDIACONTROL \_** décrivent un ensemble d’opérations génériques sur les flux de média. Les interprétations sont déterminées par le flux de média. Le périphérique de ligne doit disposer de la fonctionnalité de contrôle de média pour qu’une opération de contrôle de média soit effective.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ aucun**
</dt> <dd> <dl> <dt>



Aucune modification n’est apportée au flux multimédia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**\_Pause LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



Suspendez temporairement le flux multimédia.

La vitesse du flux multimédia est retournée à la normale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**
</dt> <dd> <dl> <dt>



La vitesse du flux multimédia est réduite par une quantité définie par le flux.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**
</dt> <dd> <dl> <dt>



La vitesse du flux multimédia est augmentée par une quantité définie par le flux.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**\_réinitialisation LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



Réinitialisez le flux multimédia. Équivalent à une fin d’entrée. Toutes les mémoires tampons sont libérées.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL \_ Resume**
</dt> <dd> <dl> <dt>



Reprend un flux de média suspendu.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ Démarrer**
</dt> <dd> <dl> <dt>



Démarrez le flux multimédia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**
</dt> <dd> <dl> <dt>



L’amplitude du flux multimédia est réduite par une quantité définie par le flux.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**
</dt> <dd> <dl> <dt>



L’amplitude du flux multimédia est retournée à la normale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**
</dt> <dd> <dl> <dt>



L’amplitude du flux multimédia est augmentée par une quantité définie par le flux.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Le contrôle de média est fourni pour améliorer les performances des actions sur les flux de média en réponse aux événements liés à la téléphonie. L’application doit normalement gérer un flux multimédia via l’API spécifique au média. La fonctionnalité de contrôle de média fournie ici n’est pas destinée à remplacer les API de média natives.

Les actions de contrôle de média peuvent être associées à la détection de chiffres, à la détection de tonalités, à la transition vers un état d’appel et à la détection d’un type de média. Consultez les fonctionnalités de l’appareil d’une ligne pour déterminer si le contrôle multimédia est disponible sur la ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




