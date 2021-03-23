---
title: Utilisation de la couche de débogage DirectML
description: La couche de débogage DirectML est un composant facultatif de développement qui vous permet de déboguer votre code DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548541"
---
# <a name="using-the-directml-debug-layer"></a>Utilisation de la couche de débogage DirectML

La couche de débogage DirectML est un composant facultatif de développement qui vous permet de déboguer votre code DirectML. La couche de débogage fait partie d’un package d’outils graphiques distinct, distribué en tant que [fonctionnalité à la demande](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (DOM). Les DOM des outils Graphics doivent être installés sur votre système pour pouvoir utiliser la couche de débogage.

Nous vous recommandons vivement d’activer la couche de débogage lors du développement d’applications à l’aide de DirectML, car elle peut fournir des informations précieuses en cas d’utilisation d’API non valide.

## <a name="installing-the-directml-debug-layer"></a>Installation de la couche de débogage DirectML

Pour installer le package facultatif des outils Graphics-à la demande (DOM), exécutez la commande suivante à partir d’une invite PowerShell d’administrateur.

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

Vous pouvez également installer le package des outils Graphics à partir des paramètres de Windows 10. Accédez à **paramètres**  >  **applications**  >  **applications & fonctionnalités** fonctionnalités  >  **facultatives**  >  **Ajouter une fonctionnalité** > puis sélectionnez **outils graphiques**.

## <a name="enabling-the-directml-debug-layer"></a>Activation de la couche de débogage DirectML

Une fois le package d’outils Graphics installé, vous pouvez activer la couche de débogage DirectML en fournissant  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) lorsque vous appelez [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).

> [!IMPORTANT]
> Vous devez d’abord activer la couche de débogage Direct3D 12. Puis *activez la* couche de débogage DirectML en appelant **DMLCreateDevice**.

Une fois que vous avez activé la couche de débogage DirectML, toutes les erreurs de DirectML ou les appels d’API non valides entraînent l’émission des informations de débogage comme sortie de débogage. Voici un exemple.

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a>Voir aussi

* [DMLCreateDevice fonction)](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [Fonctionnalités disponibles-à la demande](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [Utiliser la validation basée sur GPU avec la couche de débogage Direct3D 12](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [Référence de la couche de débogage Direct3D 12](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
