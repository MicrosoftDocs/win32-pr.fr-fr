---
description: Implémentation de IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implémentation de IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a78705fcfb53651d1099d01d17d9ddff554df9632a5cc322db229bc04d38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965008"
---
# <a name="implementing-iwicdevelopraw"></a>Implémentation de IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

L’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expose des options de traitement spécifiques au traitement d’images brutes. Tous les codecs bruts doivent prendre en charge l’interface **IWICDevelopRaw** . Certains codecs bruts peuvent ne pas être en mesure de prendre en charge tous les paramètres exposés par cette interface, mais vous devez prendre en charge tous les paramètres que votre codec est capable d’exécuter. Au minimum, chaque codec brut doit implémenter les méthodes [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) et [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .

En outre, certaines méthodes et interfaces facultatives pour d’autres codecs sont fortement recommandées pour les codecs bruts. Celles-ci incluent les méthodes [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) et [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) sur la classe de décodeur au niveau du conteneur, ainsi que l’interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur la classe de décodage au niveau de la trame.

les Paramètres définies à l’aide des méthodes [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) doivent être rendues persistantes par le codec d’une manière cohérente avec la manière dont les autres métadonnées sont conservées, mais vous ne devez jamais remplacer les paramètres « As Shot » d’origine. En rendant les métadonnées persistantes et en implémentant [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) et [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), vous permettez aux applications de traitement brutes de récupérer et d’appliquer des paramètres de traitement entre les sessions.

L’une des principales fonctions de l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) est de permettre aux développeurs d’applications de créer une interface utilisateur pour ajuster les paramètres bruts qui fonctionneront de manière aussi cohérente que possible entre les différents codecs. Supposons qu’un utilisateur final ajuste les paramètres à l’aide d’un contrôle Slider, avec ses valeurs minimale et maximale mappées aux plages minimale et maximale du paramètre. Pour prendre cela en charge, vous devez faire chaque effort pour traiter toutes les plages de paramètres comme linéaires. Pour vous assurer que les contrôles de curseur ne sont pas trop sensibles, vous devez également prendre en charge une plage aussi étendue que possible pour chaque paramètre, couvrant au moins 50% de la plage maximale possible. Par exemple, si la plage de contraste maximale possible est comprise entre le gris pur et le noir et le blanc, avec la valeur par défaut qui est mappée à 0,0, la plage minimale prise en charge par un codec est comprise entre la valeur par défaut et le gris pur sur le bas de gamme (– 1,0), au moins à mi-chemin entre la valeur par défaut et le noir et blanc pur sur le haut de gamme (+ 1,0).


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [QueryRawCapabilitiesInfo](#queryrawcapabilitiesinfo)
-   [LoadParameterSet](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Set/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/GetGamma](#setgetgamma)
-   [Set/GetSharpness](#setgetsharpness)
-   [Set/GetSaturation](#setgetsaturation)
-   [Set/GetTint](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/GetRotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) retourne l’ensemble des fonctionnalités prises en charge pour ce fichier brut. La structure [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) est définie comme suit :


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



L’énumération [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) utilisée dans cette structure est définie comme suit :


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



Le champ final est une énumération [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , définie comme suit :


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>LoadParameterSet

[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) permet à l’utilisateur de spécifier s’il faut utiliser des paramètres de capture, utiliser des paramètres modifiés par l’utilisateur ou demander au décodeur de corriger automatiquement l’image.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) retourne un **IPropertyBag2** avec le jeu de paramètres actuel. L’appelant peut ensuite passer ce paramètre à l’encodeur à utiliser comme options d’encodeur.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) et [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indiquent la compensation d’exposition à appliquer à la sortie finale. La plage valide pour EV est – 5,0 à + 5,0 s’arrête.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin

Ces fonctions fournissent toutes différentes façons d’obtenir et de définir le point blanc, en tant que valeur RVB, valeur nommée prédéfinie ou valeur Kelvin. La plage acceptable pour le Kelvin est 1 500 – 30 000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) et [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indiquent la quantité de contraste à appliquer à la sortie. La plage valide pour spécifier le contraste est comprise entre-1,0 et + 1,0, avec un contraste par défaut de 0,0.

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) et [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indiquent le gamma à appliquer. La plage valide pour gamma est 0,2 à 5,0, avec 1,0 étant la valeur par défaut. Le gamma est généralement implémenté à l’aide de la fonction de puissance gamma traditionnelle (une fonction d’alimentation linéaire avec gain d’unité). La luminosité augmente avec une valeur gamma croissante et diminue en fonction du gamma. (Notez que la valeur minimale est différente de zéro, car zéro entraînerait une erreur de division par zéro dans les calculs gamma traditionnels. La limite minimale logique est de 1/max, ce qui explique pourquoi la valeur minimale est 0,2.)

### <a name="setgetsharpness"></a>Set/GetSharpness

[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) et [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indiquent la quantité de la netteté à appliquer. La plage valide est comprise entre – 1,0 et + 1,0, avec 0,0 étant la valeur par défaut de la netteté et-1,0 qui n’indique aucune netteté.

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) et [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indiquent la quantité de saturation à appliquer. La plage valide pour spécifier la saturation est comprise entre-1,0 et + 1,0, avec une saturation normale de 0,0, – 1,0 représentant une désaturation complète et + 1,0 représentant une saturation complète.

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) et [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indiquent la teinte à appliquer, sur un biais vert/magenta. La plage valide est comprise entre – 1,0 et + 1,0, le vert étant le côté négatif de l’échelle et le magenta sur le positif. L’échelle de teinte est définie comme orthogonale à la température de couleur.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) et [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indiquent la quantité de réduction du bruit à appliquer. La plage valide est comprise entre – 1,0 et + 1,0, avec 0,0 indiquant la quantité par défaut de réduction du bruit, – 1,0 indiquant aucune réduction du bruit et + 1,0 indiquant une réduction de bruit maximale.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) spécifie le profil de couleurs à appliquer à l’image. Vous pouvez appeler [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) pour récupérer le profil de couleurs actuel.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) et [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) spécifient la courbe de tonalité à appliquer. Supposez une interpolation linéaire entre les points. **PToneCurve** est une structure [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , qui contient un tableau de structures [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) et le nombre de points dans le tableau.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



Un [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contient une valeur d’entrée et une valeur de sortie.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Lorsque l’appelant transmet **null** dans le paramètre *pToneCurve* , vous devez transmettre la taille requise pour le [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) dans le paramètre *pcbActualToneCurveBufferSize* .

### <a name="setgetrotation"></a>Set/GetRotation

[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) et [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indiquent le degré de rotation à appliquer. Une rotation de 90,0 spécifie une rotation de 90 degrés dans le sens des aiguilles d’une montre. (La différence entre l’utilisation de **SetRotation** et la définition de la rotation à l’aide de la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) est que l’angle de rotation défini à l’aide de **SetRotation** doit être rendu persistant par le codec, tandis que la définition de la rotation par le biais de **CopyPixels** fait uniquement pivoter l’image en mémoire.

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) et [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indiquent le niveau de qualité de sortie requis par l’appelant. Lorsqu’un utilisateur ajuste des paramètres, l’application doit afficher une approximation très rapide de l’apparence de l’image réelle si les modifications sont appliquées. À cet effet, l’image est généralement affichée à la résolution de l’écran ou moins, plutôt que la résolution réelle de l’image, pour fournir des commentaires immédiats à l’utilisateur. C’est lorsqu’une application demande une qualité en mode brouillon, ce qui devrait être très rapide. Lorsque l’utilisateur a apporté toutes les modifications, les affiche en mode brouillon et décide de décoder l’image complète avec les paramètres actuels, l’application demande un décodage de qualité optimal. Ce cas de figure est généralement également demandé pour l’impression. Dans le cas d’un compromis raisonnable entre la vitesse à laquelle une qualité est requise, l’application demande une qualité normale.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) inscrit une fonction de rappel que le décodeur doit appeler lorsque l’un des paramètres de traitement bruts change. La signature du [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) n’a qu’une seule méthode, appelée [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** a un seul paramètre, qui est un masque qui indique les paramètres de traitement brut modifiés.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Une opération ou est effectuée sur les valeurs suivantes pour NotificationMask.


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implémentation d’un encodeur WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



