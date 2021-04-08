---
description: La version de débogage du moteur XAudio2 valide les paramètres et fournit des messages d’avertissement et d’erreur détaillés.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Fonctionnalités de débogage XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752412"
---
# <a name="xaudio2-debugging-facilities"></a>Fonctionnalités de débogage XAudio2

La version de débogage du moteur XAudio2 valide les paramètres et fournit des messages d’avertissement et d’erreur détaillés.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Définition du niveau de journalisation du débogage au moment de l’exécution

Vous pouvez définir le niveau des informations de débogage affichées par XAudio2 à tout moment en remplissant une structure [**de \_ \_ configuration de débogage XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) avec les indicateurs du niveau de journalisation souhaité, puis passer la structure à la méthode [**IXAudio2 :: SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) . Les valeurs passées à la méthode **IXAudio2 :: SetDebugConfiguration** remplacent toujours toutes les valeurs par défaut qui ont été définies dans le Registre Windows.

## <a name="debug-support"></a>Prise en charge du débogage

Les fonctionnalités de débogage sont toujours disponibles pour XAUDIO2 dans Windows 8.

Pour les versions du kit de développement logiciel (SDK) DirectX de XAUDIO2, vous devez utiliser le **\_ \_ moteur de débogage XAUDIO2** lors de la création de l’objet XAUDIO2 avec [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) et le runtime SDK développeur DirectX doit être installé sur le système pour que le débogage soit pris en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de débogage](debugging-facilities.md)
</dt> <dt>

[Référence de programmation XAudio2](programming-reference.md)
</dt> </dl>

 

 
