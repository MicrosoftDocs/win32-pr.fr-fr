---
title: EnableDCOM
description: Contrôle l’activation globale et les stratégies d’appel de l’ordinateur. Seuls les administrateurs et le système ont un accès complet à cette partie du Registre. Tous les autres utilisateurs disposent d’un accès en lecture seule.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valeur de Registre EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74aea79cf600aad4407b96b5c4a10e8f44633a1c928f8b7e376c192b108cb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793598"
---
# <a name="enabledcom"></a>EnableDCOM

Contrôle l’activation globale et les stratégies d’appel de l’ordinateur. Seuls les administrateurs et le système ont un accès complet à cette partie du Registre. Tous les autres utilisateurs disposent d’un accès en lecture seule.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** .



| Valeur    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (ou n) | Aucun client distant ne peut lancer des serveurs ou se connecter à des objets sur cet ordinateur. Les clients locaux ne peuvent pas accéder aux serveurs DCOM distants ; tout le trafic DCOM est bloqué. Le lancement local de code de classe et la connexion aux objets sont autorisés par classe en fonction de la valeur et des autorisations d’accès de la valeur de Registre [**LaunchPermission**](launchpermission.md) de la classe et de la valeur de Registre [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale. |
| Y (ou y) | Le lancement de serveurs et la connexion aux objets par des clients distants sont autorisés par classe en fonction de la valeur et des autorisations d’accès de la valeur de Registre [**LaunchPermission**](launchpermission.md) de la classe et de la valeur de Registre [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale.                                                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




