---
description: Le programme SndVol32.exe contrôle les paramètres de volume de votre système. Pour afficher ce contrôle du volume, accédez au panneau de configuration et démarrez sons et périphériques audio. Accédez à volume de l’appareil, puis cliquez sur avancé.
ms.assetid: 20e7fb8a-d0a5-46fa-9813-567fa4f57e8f
title: SndVol32.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2934c9b81a82a127c7fe99b436d6fc20b011684b96e78ebc26d5ce36a787e24d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044589"
---
# <a name="sndvol32exe"></a>SndVol32.exe

Le programme SndVol32.exe contrôle les paramètres de volume de votre système. Pour afficher ce contrôle du volume, accédez au panneau de configuration et démarrez sons et périphériques audio. Accédez à **volume** de l’appareil, puis cliquez sur **avancé**.

Pour exécuter ce programme avec des arguments de ligne de commande, accédez au menu **Démarrer** , cliquez sur **exécuter**, puis tapez la commande suivante.

**SndVol32.exe \[ -R \| -D** *\] n ** * **

<dl> <dt>

<span id="-R"></span><span id="-r"></span>-R
</dt> <dd>

Démarre l’application en mode d’enregistrement.

</dd> <dt>

<span id="-D_n"></span><span id="-d_n"></span><span id="-D_N"></span>-D *n*
</dt> <dd>

Spécifie un identificateur d’appareil.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce programme est le contrôle du volume et du mélangeur audio natif inclus dans Windows ; elle n’est pas disponible au téléchargement à partir de Microsoft. le programme est généralement installé dans le répertoire suivant : C : \\ Windows \\ System32.

pour localiser ce fichier sur votre système, ouvrez Windows Explorer, cliquez sur le bouton **rechercher** , puis sélectionnez **tous les fichiers et dossiers**. Tapez le nom du fichier (SndVol32.exe) dans la première ligne disponible, puis cliquez sur le bouton **Rechercher** .

Pour plus d’informations sur l’utilisation de ce contrôle, démarrez le programme et sélectionnez **aide**. Notez qu’il n’existe aucun moyen d’accéder par programmation aux fonctionnalités de ce programme.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[SysTray et SndVol32](https://msdn.microsoft.com/library/ms790410.aspx)
</dt> </dl>

 

 



