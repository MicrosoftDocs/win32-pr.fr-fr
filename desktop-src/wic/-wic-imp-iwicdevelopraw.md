---
description: Implémentation de IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implémentation de IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210819"
---
# <a name="implementing-iwicdevelopraw"></a><span data-ttu-id="647c6-103">Implémentation de IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="647c6-103">Implementing IWICDevelopRaw</span></span>

## <a name="iwicdevelopraw"></a><span data-ttu-id="647c6-104">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="647c6-104">IWICDevelopRaw</span></span>

<span data-ttu-id="647c6-105">L’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expose des options de traitement spécifiques au traitement d’images brutes.</span><span class="sxs-lookup"><span data-stu-id="647c6-105">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface exposes processing options specific to raw image processing.</span></span> <span data-ttu-id="647c6-106">Tous les codecs bruts doivent prendre en charge l’interface **IWICDevelopRaw** .</span><span class="sxs-lookup"><span data-stu-id="647c6-106">All raw codecs must support the **IWICDevelopRaw** interface.</span></span> <span data-ttu-id="647c6-107">Certains codecs bruts peuvent ne pas être en mesure de prendre en charge tous les paramètres exposés par cette interface, mais vous devez prendre en charge tous les paramètres que votre codec est capable d’exécuter.</span><span class="sxs-lookup"><span data-stu-id="647c6-107">Some raw codecs may not be able to support every setting exposed by this interface, but you should support all the settings that your codec is capable of performing.</span></span> <span data-ttu-id="647c6-108">Au minimum, chaque codec brut doit implémenter les méthodes [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) et [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .</span><span class="sxs-lookup"><span data-stu-id="647c6-108">At minimum, every raw codec must implement the [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) methods.</span></span>

<span data-ttu-id="647c6-109">En outre, certaines méthodes et interfaces facultatives pour d’autres codecs sont fortement recommandées pour les codecs bruts.</span><span class="sxs-lookup"><span data-stu-id="647c6-109">Additionally, some methods and interfaces that are optional for other codecs are strongly recommended for raw codecs.</span></span> <span data-ttu-id="647c6-110">Celles-ci incluent les méthodes [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) et [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) sur la classe de décodeur au niveau du conteneur, ainsi que l’interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur la classe de décodage au niveau de la trame.</span><span class="sxs-lookup"><span data-stu-id="647c6-110">These include the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) and [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) methods on the container-level decoder class, and the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface on the frame-level decode class.</span></span>

<span data-ttu-id="647c6-111">Les paramètres définis à l’aide des méthodes [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) doivent être rendus persistants par le codec d’une manière cohérente avec la manière dont les autres métadonnées sont conservées, mais vous ne devez jamais remplacer les paramètres « As Shot » d’origine.</span><span class="sxs-lookup"><span data-stu-id="647c6-111">Settings set by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) methods should be persisted by the codec in a way that’s consistent with the way other metadata is persisted, but you should never overwrite the original "As Shot" settings.</span></span> <span data-ttu-id="647c6-112">En rendant les métadonnées persistantes et en implémentant [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) et [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), vous permettez aux applications de traitement brutes de récupérer et d’appliquer des paramètres de traitement entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="647c6-112">By persisting the metadata and implementing [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) and [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), you enable raw processing applications to retrieve and apply processing settings across sessions.</span></span>

<span data-ttu-id="647c6-113">L’une des principales fonctions de l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) est de permettre aux développeurs d’applications de créer une interface utilisateur pour ajuster les paramètres bruts qui fonctionneront de manière aussi cohérente que possible entre les différents codecs.</span><span class="sxs-lookup"><span data-stu-id="647c6-113">A main purpose of the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface is to enable application developers to build a user interface for adjusting raw parameters that will work as consistently as possible across different codecs.</span></span> <span data-ttu-id="647c6-114">Supposons qu’un utilisateur final ajuste les paramètres à l’aide d’un contrôle Slider, avec ses valeurs minimale et maximale mappées aux plages minimale et maximale du paramètre.</span><span class="sxs-lookup"><span data-stu-id="647c6-114">Assume that an end user will adjust the parameters by using a slider control, with its minimum and maximum values mapped to the minimum and maximum ranges for the parameter.</span></span> <span data-ttu-id="647c6-115">Pour prendre cela en charge, vous devez faire chaque effort pour traiter toutes les plages de paramètres comme linéaires.</span><span class="sxs-lookup"><span data-stu-id="647c6-115">To support this, you should make every effort to treat all parameter ranges as linear.</span></span> <span data-ttu-id="647c6-116">Pour vous assurer que les contrôles de curseur ne sont pas trop sensibles, vous devez également prendre en charge une plage aussi étendue que possible pour chaque paramètre, couvrant au moins 50% de la plage maximale possible.</span><span class="sxs-lookup"><span data-stu-id="647c6-116">To ensure that the slider controls aren’t overly sensitive, you should also support as broad a range as possible for each parameter, covering at least 50 percent of the maximum possible range.</span></span> <span data-ttu-id="647c6-117">Par exemple, si la plage de contraste maximale possible est comprise entre le gris pur et le noir et le blanc, avec la valeur par défaut qui est mappée à 0,0, la plage minimale prise en charge par un codec est comprise entre la valeur par défaut et le gris pur sur le bas de gamme (– 1,0), au moins à mi-chemin entre la valeur par défaut et le noir et blanc pur sur le haut de gamme (+ 1,0).</span><span class="sxs-lookup"><span data-stu-id="647c6-117">For example, if the maximum possible range of contrast is from pure gray to pure black and white, with the default value being mapped to 0.0, the minimum range supported by a codec would be from at least halfway between the default value and pure gray on the low end (–1.0), to at least halfway between the default value and pure black and white on the high end (+1.0).</span></span>


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



-   [<span data-ttu-id="647c6-118">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="647c6-118">QueryRawCapabilitiesInfo</span></span>](#queryrawcapabilitiesinfo)
-   [<span data-ttu-id="647c6-119">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="647c6-119">LoadParameterSet</span></span>](#loadparameterset)
-   [<span data-ttu-id="647c6-120">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="647c6-120">GetCurrentParameterSet</span></span>](#getcurrentparameterset)
-   [<span data-ttu-id="647c6-121">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="647c6-121">Set/GetExposureCompensation</span></span>](#setgetexposurecompensation)
-   [<span data-ttu-id="647c6-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="647c6-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [<span data-ttu-id="647c6-123">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="647c6-123">Set/GetContrast</span></span>](#setgetcontrast)
-   [<span data-ttu-id="647c6-124">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="647c6-124">Set/GetGamma</span></span>](#setgetgamma)
-   [<span data-ttu-id="647c6-125">Set/GetSharpness</span><span class="sxs-lookup"><span data-stu-id="647c6-125">Set/GetSharpness</span></span>](#setgetsharpness)
-   [<span data-ttu-id="647c6-126">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="647c6-126">Set/GetSaturation</span></span>](#setgetsaturation)
-   [<span data-ttu-id="647c6-127">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="647c6-127">Set/GetTint</span></span>](#setgettint)
-   [<span data-ttu-id="647c6-128">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="647c6-128">Set/GetNoiseReduction</span></span>](#setgetnoisereduction)
-   [<span data-ttu-id="647c6-129">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="647c6-129">SetDestinationColorContext</span></span>](#setdestinationcolorcontext)
-   [<span data-ttu-id="647c6-130">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="647c6-130">Set/GetToneCurve</span></span>](#setgettonecurve)
-   [<span data-ttu-id="647c6-131">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="647c6-131">Set/GetRotation</span></span>](#setgetrotation)
-   [<span data-ttu-id="647c6-132">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="647c6-132">Set/GetRenderMode</span></span>](#setgetrendermode)
-   [<span data-ttu-id="647c6-133">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="647c6-133">SetNotificationCallback</span></span>](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a><span data-ttu-id="647c6-134">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="647c6-134">QueryRawCapabilitiesInfo</span></span>

<span data-ttu-id="647c6-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) retourne l’ensemble des fonctionnalités prises en charge pour ce fichier brut.</span><span class="sxs-lookup"><span data-stu-id="647c6-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) returns the set of supported capabilities for this raw file.</span></span> <span data-ttu-id="647c6-136">La structure [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="647c6-136">The [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) structure is defined as follows:</span></span>


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



<span data-ttu-id="647c6-137">L’énumération [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) utilisée dans cette structure est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="647c6-137">The [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) enumeration used in this structure is defined as:</span></span>


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



<span data-ttu-id="647c6-138">Le champ final est une énumération [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="647c6-138">The final field is a [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) enumeration, defined as:</span></span>


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a><span data-ttu-id="647c6-139">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="647c6-139">LoadParameterSet</span></span>

<span data-ttu-id="647c6-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) permet à l’utilisateur de spécifier s’il faut utiliser des paramètres de capture, utiliser des paramètres modifiés par l’utilisateur ou demander au décodeur de corriger automatiquement l’image.</span><span class="sxs-lookup"><span data-stu-id="647c6-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) enables the user to specify whether to use As Shot settings, use user-adjusted settings, or request the decoder to auto-correct the image.</span></span>


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a><span data-ttu-id="647c6-141">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="647c6-141">GetCurrentParameterSet</span></span>

<span data-ttu-id="647c6-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) retourne un **IPropertyBag2** avec le jeu de paramètres actuel.</span><span class="sxs-lookup"><span data-stu-id="647c6-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) returns an **IPropertyBag2** with the current parameter set.</span></span> <span data-ttu-id="647c6-143">L’appelant peut ensuite passer ce paramètre à l’encodeur à utiliser comme options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="647c6-143">The caller can then pass this parameter set to the encoder to use as the encoder options.</span></span>

### <a name="setgetexposurecompensation"></a><span data-ttu-id="647c6-144">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="647c6-144">Set/GetExposureCompensation</span></span>

<span data-ttu-id="647c6-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) et [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indiquent la compensation d’exposition à appliquer à la sortie finale.</span><span class="sxs-lookup"><span data-stu-id="647c6-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) and [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicate the exposure compensation to apply to the final output.</span></span> <span data-ttu-id="647c6-146">La plage valide pour EV est – 5,0 à + 5,0 s’arrête.</span><span class="sxs-lookup"><span data-stu-id="647c6-146">The valid range for EV is –5.0 to +5.0 stops.</span></span>

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a><span data-ttu-id="647c6-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="647c6-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>

<span data-ttu-id="647c6-148">Ces fonctions fournissent toutes différentes façons d’obtenir et de définir le point blanc, en tant que valeur RVB, valeur nommée prédéfinie ou valeur Kelvin.</span><span class="sxs-lookup"><span data-stu-id="647c6-148">These functions all provide ways to get and set the white point, either as an RGB value, a preset named value, or as a Kelvin value.</span></span> <span data-ttu-id="647c6-149">La plage acceptable pour le Kelvin est 1 500 – 30 000.</span><span class="sxs-lookup"><span data-stu-id="647c6-149">The acceptable range for Kelvin is 1,500 – 30,000.</span></span>

### <a name="setgetcontrast"></a><span data-ttu-id="647c6-150">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="647c6-150">Set/GetContrast</span></span>

<span data-ttu-id="647c6-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) et [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indiquent la quantité de contraste à appliquer à la sortie.</span><span class="sxs-lookup"><span data-stu-id="647c6-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) and [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicate the amount of contrast to apply to the output.</span></span> <span data-ttu-id="647c6-152">La plage valide pour spécifier le contraste est comprise entre-1,0 et + 1,0, avec un contraste par défaut de 0,0.</span><span class="sxs-lookup"><span data-stu-id="647c6-152">The valid range to specify contrast is –1.0 to +1.0, with the default contrast being 0.0.</span></span>

### <a name="setgetgamma"></a><span data-ttu-id="647c6-153">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="647c6-153">Set/GetGamma</span></span>

<span data-ttu-id="647c6-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) et [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indiquent le gamma à appliquer.</span><span class="sxs-lookup"><span data-stu-id="647c6-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) and [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicate the Gamma to apply.</span></span> <span data-ttu-id="647c6-155">La plage valide pour gamma est 0,2 à 5,0, avec 1,0 étant la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="647c6-155">The valid range for Gamma is 0.2 to 5.0, with 1.0 being the default.</span></span> <span data-ttu-id="647c6-156">Le gamma est généralement implémenté à l’aide de la fonction de puissance gamma traditionnelle (une fonction d’alimentation linéaire avec gain d’unité).</span><span class="sxs-lookup"><span data-stu-id="647c6-156">Gamma typically is implemented using the traditional Gamma power function (a linear power function with unity gain).</span></span> <span data-ttu-id="647c6-157">La luminosité augmente avec une valeur gamma croissante et diminue en fonction du gamma.</span><span class="sxs-lookup"><span data-stu-id="647c6-157">Brightness is increased with increasing Gamma and decreased as Gamma approaches zero.</span></span> <span data-ttu-id="647c6-158">(Notez que la valeur minimale est différente de zéro, car zéro entraînerait une erreur de division par zéro dans les calculs gamma traditionnels.</span><span class="sxs-lookup"><span data-stu-id="647c6-158">(Note that the minimum value is non-zero, because zero would result in a divide-by-zero error in traditional Gamma calculations.</span></span> <span data-ttu-id="647c6-159">La limite minimale logique est de 1/max, ce qui explique pourquoi la valeur minimale est 0,2.)</span><span class="sxs-lookup"><span data-stu-id="647c6-159">The logical minimum limit is 1/max, which is why the minimum is 0.2.)</span></span>

### <a name="setgetsharpness"></a><span data-ttu-id="647c6-160">Set/GetSharpness</span><span class="sxs-lookup"><span data-stu-id="647c6-160">Set/GetSharpness</span></span>

<span data-ttu-id="647c6-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) et [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indiquent la quantité de la netteté à appliquer.</span><span class="sxs-lookup"><span data-stu-id="647c6-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) and [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicate the amount of sharpening to apply.</span></span> <span data-ttu-id="647c6-162">La plage valide est comprise entre – 1,0 et + 1,0, avec 0,0 étant la valeur par défaut de la netteté et-1,0 qui n’indique aucune netteté.</span><span class="sxs-lookup"><span data-stu-id="647c6-162">The valid range is –1.0 to +1.0, with 0.0 being the default amount of sharpening, and –1.0 indicating no sharpening at all.</span></span>

### <a name="setgetsaturation"></a><span data-ttu-id="647c6-163">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="647c6-163">Set/GetSaturation</span></span>

<span data-ttu-id="647c6-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) et [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indiquent la quantité de saturation à appliquer.</span><span class="sxs-lookup"><span data-stu-id="647c6-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) and [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicate the amount of saturation to apply.</span></span> <span data-ttu-id="647c6-165">La plage valide pour spécifier la saturation est comprise entre-1,0 et + 1,0, avec une saturation normale de 0,0, – 1,0 représentant une désaturation complète et + 1,0 représentant une saturation complète.</span><span class="sxs-lookup"><span data-stu-id="647c6-165">The valid range to specify saturation is –1.0 to +1.0, with 0.0 being normal saturation, –1.0 representing complete desaturation, and +1.0 representing full saturation.</span></span>

### <a name="setgettint"></a><span data-ttu-id="647c6-166">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="647c6-166">Set/GetTint</span></span>

<span data-ttu-id="647c6-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) et [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indiquent la teinte à appliquer, sur un biais vert/magenta.</span><span class="sxs-lookup"><span data-stu-id="647c6-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) and [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicate the tint to apply, on a green/magenta bias.</span></span> <span data-ttu-id="647c6-168">La plage valide est comprise entre – 1,0 et + 1,0, le vert étant le côté négatif de l’échelle et le magenta sur le positif.</span><span class="sxs-lookup"><span data-stu-id="647c6-168">The valid range is –1.0 to +1.0, with green being on the negative side of the scale and magenta on the positive.</span></span> <span data-ttu-id="647c6-169">L’échelle de teinte est définie comme orthogonale à la température de couleur.</span><span class="sxs-lookup"><span data-stu-id="647c6-169">The tint scale is defined as orthogonal to color temperature.</span></span>

### <a name="setgetnoisereduction"></a><span data-ttu-id="647c6-170">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="647c6-170">Set/GetNoiseReduction</span></span>

<span data-ttu-id="647c6-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) et [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indiquent la quantité de réduction du bruit à appliquer.</span><span class="sxs-lookup"><span data-stu-id="647c6-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) and [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicate the amount of noise reduction to apply.</span></span> <span data-ttu-id="647c6-172">La plage valide est comprise entre – 1,0 et + 1,0, avec 0,0 indiquant la quantité par défaut de réduction du bruit, – 1,0 indiquant aucune réduction du bruit et + 1,0 indiquant une réduction de bruit maximale.</span><span class="sxs-lookup"><span data-stu-id="647c6-172">The valid range to is –1.0 to +1.0, with 0.0 indicating the default amount of noise reduction, –1.0 indicating no noise reduction and +1.0 indicating maximum noise reduction.</span></span>

### <a name="setdestinationcolorcontext"></a><span data-ttu-id="647c6-173">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="647c6-173">SetDestinationColorContext</span></span>

<span data-ttu-id="647c6-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) spécifie le profil de couleurs à appliquer à l’image.</span><span class="sxs-lookup"><span data-stu-id="647c6-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifies the color profile to apply to the image.</span></span> <span data-ttu-id="647c6-175">Vous pouvez appeler [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) pour récupérer le profil de couleurs actuel.</span><span class="sxs-lookup"><span data-stu-id="647c6-175">You can call [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) to retrieve the current color profile.</span></span>

### <a name="setgettonecurve"></a><span data-ttu-id="647c6-176">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="647c6-176">Set/GetToneCurve</span></span>

<span data-ttu-id="647c6-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) et [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) spécifient la courbe de tonalité à appliquer.</span><span class="sxs-lookup"><span data-stu-id="647c6-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) and [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specify the tone curve to apply.</span></span> <span data-ttu-id="647c6-178">Supposez une interpolation linéaire entre les points.</span><span class="sxs-lookup"><span data-stu-id="647c6-178">Assume linear interpolation between points.</span></span> <span data-ttu-id="647c6-179">**PToneCurve** est une structure [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , qui contient un tableau de structures [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) et le nombre de points dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="647c6-179">The **pToneCurve** is a [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) structure, which contains an array of [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) structures, and a count of the number of points in the array.</span></span>


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



<span data-ttu-id="647c6-180">Un [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contient une valeur d’entrée et une valeur de sortie.</span><span class="sxs-lookup"><span data-stu-id="647c6-180">A [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contains an input value and an output value.</span></span>


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



<span data-ttu-id="647c6-181">Lorsque l’appelant transmet **null** dans le paramètre *pToneCurve* , vous devez transmettre la taille requise pour le [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) dans le paramètre *pcbActualToneCurveBufferSize* .</span><span class="sxs-lookup"><span data-stu-id="647c6-181">When the caller passes **NULL** in the *pToneCurve* parameter, you should pass back the required size for the [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) in the *pcbActualToneCurveBufferSize* parameter.</span></span>

### <a name="setgetrotation"></a><span data-ttu-id="647c6-182">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="647c6-182">Set/GetRotation</span></span>

<span data-ttu-id="647c6-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) et [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indiquent le degré de rotation à appliquer.</span><span class="sxs-lookup"><span data-stu-id="647c6-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) and [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicate the degree of rotation to apply.</span></span> <span data-ttu-id="647c6-184">Une rotation de 90,0 spécifie une rotation de 90 degrés dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="647c6-184">A rotation of 90.0 would specify a rotation of 90 degrees clockwise.</span></span> <span data-ttu-id="647c6-185">(La différence entre l’utilisation de **SetRotation** et la définition de la rotation à l’aide de la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) est que l’angle de rotation défini à l’aide de **SetRotation** doit être rendu persistant par le codec, tandis que la définition de la rotation par le biais de **CopyPixels** fait uniquement pivoter l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="647c6-185">(The difference between using **SetRotation** and setting rotation using the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method is that the rotation angle set using **SetRotation** should be persisted by the codec, while setting rotation through **CopyPixels** only rotates the image in memory.</span></span>

### <a name="setgetrendermode"></a><span data-ttu-id="647c6-186">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="647c6-186">Set/GetRenderMode</span></span>

<span data-ttu-id="647c6-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) et [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indiquent le niveau de qualité de sortie requis par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="647c6-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicate the quality level of output the caller requires.</span></span> <span data-ttu-id="647c6-188">Lorsqu’un utilisateur ajuste des paramètres, l’application doit afficher une approximation très rapide de l’apparence de l’image réelle si les modifications sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="647c6-188">When a user is adjusting parameters, the application should display a very fast approximation of what the actual image will look like if the changes are applied.</span></span> <span data-ttu-id="647c6-189">À cet effet, l’image est généralement affichée à la résolution de l’écran ou moins, plutôt que la résolution réelle de l’image, pour fournir des commentaires immédiats à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="647c6-189">For this purpose, the image is usually displayed at screen resolution or less, rather than the actual image resolution, to provide immediate feedback to the user.</span></span> <span data-ttu-id="647c6-190">C’est lorsqu’une application demande une qualité en mode brouillon, ce qui devrait être très rapide.</span><span class="sxs-lookup"><span data-stu-id="647c6-190">This is when an application would request Draft Mode quality, so this should be very fast.</span></span> <span data-ttu-id="647c6-191">Lorsque l’utilisateur a apporté toutes les modifications, les affiche en mode brouillon et décide de décoder l’image complète avec les paramètres actuels, l’application demande un décodage de qualité optimal.</span><span class="sxs-lookup"><span data-stu-id="647c6-191">When the user has made all changes, previewed them in draft mode, and decided to decode the full image with the current settings, the application requests a Best Quality decode.</span></span> <span data-ttu-id="647c6-192">Ce cas de figure est généralement également demandé pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="647c6-192">This is usually also requested for printing.</span></span> <span data-ttu-id="647c6-193">Dans le cas d’un compromis raisonnable entre la vitesse à laquelle une qualité est requise, l’application demande une qualité normale.</span><span class="sxs-lookup"><span data-stu-id="647c6-193">Where a reasonable tradeoff between speed an quality is required, the application requests Normal Quality.</span></span>


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a><span data-ttu-id="647c6-194">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="647c6-194">SetNotificationCallback</span></span>

<span data-ttu-id="647c6-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) inscrit une fonction de rappel que le décodeur doit appeler lorsque l’un des paramètres de traitement bruts change.</span><span class="sxs-lookup"><span data-stu-id="647c6-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registers a callback function for the decoder to call when any of the Raw processing parameters change.</span></span> <span data-ttu-id="647c6-196">La signature du [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) n’a qu’une seule méthode, appelée [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span><span class="sxs-lookup"><span data-stu-id="647c6-196">The signature for the [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) has only one method, called [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span></span> <span data-ttu-id="647c6-197">**Notify** a un seul paramètre, qui est un masque qui indique les paramètres de traitement brut modifiés.</span><span class="sxs-lookup"><span data-stu-id="647c6-197">**Notify** has a single parameter, which is a mask that indicates which of the raw processing parameters have changed.</span></span>


```C++
HRESULT Notify ( UINT NotificationMask );
```



<span data-ttu-id="647c6-198">Une opération ou est effectuée sur les valeurs suivantes pour NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="647c6-198">An OR operation is performed on the following values for the NotificationMask.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="647c6-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="647c6-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="647c6-200">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="647c6-200">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="647c6-201">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="647c6-201">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

<span data-ttu-id="647c6-202">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="647c6-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="647c6-203">Implémentation de IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="647c6-203">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="647c6-204">Implémentation d’un encodeur WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="647c6-204">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="647c6-205">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="647c6-205">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="647c6-206">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="647c6-206">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



