---
description: Crée un objet de contexte qui décrit le périphérique tablette spécifié.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'ITablet :: CreateContext, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868285"
---
# <a name="itabletcreatecontext-method"></a>ITablet :: CreateContext, méthode

Crée un objet de contexte qui décrit le périphérique tablette spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Fenêtre à laquelle le contexte de tablette sera attaché.

</dd> <dt>

*prcInput* \[ dans\]
</dt> <dd>

\[dans, unique\]

Rectangle de saisie d’encre.

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Indicateurs qui définissent des options de contexte de tablette.

</dd> <dt>

*pTCS* \[ dans\]
</dt> <dd>

\[dans, unique\]

Informations détaillées sur le contexte de tablette à créer.

</dd> <dt>

*cet* \[ dans\]
</dt> <dd>

Valeur qui active ou désactive les messages de contexte envoyés à la fenêtre.

</dd> <dt>

*ppCtx* \[ à\]
</dt> <dd>

Pointeur vers le contexte de tablette nouvellement créé.

</dd> <dt>

*pTcid* \[ in, out\]
</dt> <dd>

Valeur qui identifie de façon unique la tablette.

</dd> <dt>

*ppPD* \[ in, out\]
</dt> <dd>

Pointeur vers des informations sur les données contenues dans chaque paquet.

</dd> <dt>

*pSink* \[ dans\]
</dt> <dd>

Objet [**ITabletEventSink**](itableteventsink.md) dans lequel les messages de notification seront envoyés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

En règle générale, une application obtient les valeurs par défaut à partir de la [**méthode ITablet :: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifie les valeurs en fonction de leurs besoins, puis passe la structure des paramètres modifiés à la **méthode ITablet :: CreateContext**.

> [!Note]  
> Vous devez implémenter l' [**interface ITabletEventSink**](itableteventsink.md) lors de l’appel de la **méthode ITablet :: CreateContext**.

 

Le paramètre *dwOptions* est un jeu d’indicateurs binaires qui décrivent les options de contexte. Le tableau suivant décrit ces indicateurs.



| Nom de l’indicateur                                | Valeur                                                                                                                                                                                         | Description                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_marge TCXO<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Spécifie que le contexte d’entrée sur la tablette aura une marge. La marge est une zone située en dehors de la zone d’entrée spécifiée où les événements sont mappés sur le bord de la zone d’entrée. Cette fonctionnalité facilite l’entrée des points à la périphérie du contexte.<br/> |
| préhook TCXO \_<br/>                 | 0x00000002<br/>                                                                                                                                                                         | Le préhook obtient les paquets avant les contextes standard et les posthooks. Ils obtiennent des paquets dans l’ordre de leur création.<br/>                                                                                                                                                  |
| \_État du curseur TCXO \_<br/>           | 0x00000004<br/>                                                                                                                                                                         | Le TC renverra des paquets même si le curseur est en place. Par défaut, TC retourne des paquets uniquement lorsque le curseur est en aval.<br/>                                                                                                                                       |
| TCXO \_ aucun \_ curseur en \_ dessous<br/>        | 0x00000008<br/>                                                                                                                                                                         | Le TC ne retourne pas de paquets lorsque le curseur est en aval.<br/>                                                                                                                                                                                                       |
| TCXO \_ non \_ intégré<br/>         | 0x00000010<br/>                                                                                                                                                                         | Le contexte ne sera pas intégré.<br/>                                                                                                                                                                                                                           |
| TCXO \_ POSTHOOK<br/>                | 0x00000020<br/>                                                                                                                                                                         | Posthooks obtient des paquets après des contextes de tablette normaux mais avant le contexte système. Ils obtiennent des paquets dans l’ordre inverse de leur création.<br/>                                                                                                                   |
| TCXO ne pas \_ \_ afficher le \_ curseur<br/>      | 0x00000080<br/>                                                                                                                                                                         | Le TC ne définit pas la position du curseur.<br/>                                                                                                                                                                                                                      |
| TCXO ne pas \_ \_ valider les \_ TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | TC ne valide pas les GUID transmis dans les paramètres de contexte de tablette par rapport aux propriétés prises en charge de l’appareil.<br/>                                                                                                                                      |
| TCXO \_ autoriser les \_ raccourcis<br/>           | 0x00000400<br/>                                                                                                                                                                         | Le TC autorisera la détection de mouvement (par défaut, cette opération est autorisée uniquement dans les contextes système) et le client obtiendra les \_ événements de scintillement se.<br/>                                                                                                               |
| TCXO \_ autoriser \_ les \_ clics de commentaires<br/>   | 0x00000800<br/>                                                                                                                                                                         | Le TC permettra d’afficher les commentaires du stylet. Par défaut, cette valeur est autorisée uniquement dans les contextes système.<br/>                                                                                                                                                              |
| TCXO \_ autoriser les \_ Commentaires \_ Barrel<br/> | 0x00001000<br/>                                                                                                                                                                         | Le TC permettra d’afficher les commentaires du stylet. Par défaut, cette valeur est autorisée uniquement dans les contextes système.<br/>                                                                                                                                                              |
| TCXO \_ tout<br/>                     | TCXO \_ Margin \| TCXO \_ préhook \| TCXO \_ État du curseur \_ \| TCXO \_ aucun \_ curseur vers le faible TCXO non intégré TCXO POSTHOOK TCXO ne pas \_ \| \_ afficher le \_ \| \_ \| \_ \_ \_ curseur \| TCXO \_ \_ \_ ne pas valider les TCS<br/> | Toutes les options de contexte de tablette définies.<br/>                                                                                                                                                                                                                           |
| \_Hook TCXO<br/>                    | TCXO \_ prehook \| TCXO \_ POSTHOOK<br/>                                                                                                                                                    | Combine les fonctionnalités de pré-Hook et de postconnexion.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> <dt>

[**\_Énumération des types d’activation de contexte \_**](context-enable-type.md)
</dt> <dt>

[**Structure des paramètres de \_ contexte de tablette \_**](tablet-context-settings.md)
</dt> <dt>

[**Structure de la description du paquet \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




