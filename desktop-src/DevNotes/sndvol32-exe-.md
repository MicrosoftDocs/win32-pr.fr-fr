---
description: Le programme SndVol32.exe contrôle les paramètres de volume de votre système. Pour afficher ce contrôle du volume, accédez au panneau de configuration et démarrez sons et périphériques audio. Accédez à volume de l’appareil, puis cliquez sur avancé.
ms.assetid: 20e7fb8a-d0a5-46fa-9813-567fa4f57e8f
title: SndVol32.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24df0f5d6ec25b1843f8aa195c2b365d3f11814
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950365"
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

## <a name="remarks"></a>Notes

Ce programme est le contrôle du volume et du mélangeur audio natif inclus dans Windows. elle n’est pas disponible au téléchargement à partir de Microsoft. Le programme est généralement installé dans le répertoire suivant : C : \\ Windows \\ system32.

Pour localiser ce fichier sur votre système, ouvrez l’Explorateur Windows, cliquez sur le bouton **Rechercher** , puis sélectionnez **tous les fichiers et dossiers**. Tapez le nom du fichier (SndVol32.exe) dans la première ligne disponible, puis cliquez sur le bouton **Rechercher** .

Pour plus d’informations sur l’utilisation de ce contrôle, démarrez le programme et sélectionnez **aide**. Notez qu’il n’existe aucun moyen d’accéder par programmation aux fonctionnalités de ce programme.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[SysTray et SndVol32](https://msdn.microsoft.com/library/ms790410.aspx)
</dt> </dl>

 

 



