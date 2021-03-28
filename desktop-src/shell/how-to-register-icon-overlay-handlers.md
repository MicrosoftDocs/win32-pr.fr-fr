---
description: En plus de l’inscription du modèle COM (Component Object Model) normal, les étapes suivantes doivent être effectuées pour pouvoir inscrire des gestionnaires de superposition d’icône.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Comment inscrire des gestionnaires de superposition d’icône
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb58747adc9b754481f43fec825a4588e1606ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991552"
---
# <a name="how-to-register-icon-overlay-handlers"></a>Comment inscrire des gestionnaires de superposition d’icône

En plus de l’inscription du modèle COM (Component Object Model) normal, les étapes suivantes doivent être effectuées pour pouvoir inscrire des gestionnaires de superposition d’icône.

## <a name="instructions"></a>Instructions

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Étape 1 : créer une sous-clé nommée pour le gestionnaire sous cette clé

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Étape 2 : définir la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) de l’objet

L’exemple suivant montre comment enregistrer un gestionnaire de superposition d’icône nommé MyOverlay.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 



